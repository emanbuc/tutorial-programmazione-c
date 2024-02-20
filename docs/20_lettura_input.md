# Lettura degli input degli utenti

Gestire gli input dell'utente in C è un'operazione fondamentale per la realizzazione di programmi interattivi. In questo tutorial vedremo come gestire gli input dell'utente utilizzando la funzione scanf() e come evitare problemi di sicurezza con la funzione fgets().  
   
La funzione scanf()  
La funzione scanf() è utilizzata per leggere gli input dell'utente da stdin (standard input) e assegnarli a variabili in C. La sintassi di base di scanf() è la seguente:  
   
```  
scanf(formato, arg1, arg2, ...)  
```  
   
dove il parametro formato definisce il tipo di dato dell'input che deve essere letto, mentre gli argomenti successivi sono le variabili in cui memorizzare i valori letti. Ad esempio, per leggere un intero dall'utente e memorizzarlo in una variabile x, utilizziamo la seguente istruzione:  
   
```  
scanf("%d", &x);  
```  
   
Dove "%d" indica che l'input deve essere un intero e "&x" è l'indirizzo della variabile x.  
   
La funzione fgets()  
La funzione fgets() è una alternativa più sicura di scanf() per leggere gli input dell'utente. fgets() legge una stringa di input da stdin e la memorizza in un buffer di caratteri. La sintassi di base di fgets() è la seguente:  
   
```  
fgets(buffer, size, stdin);  
```  
   
dove buffer è il nome della variabile in cui memorizzare la stringa di input, size è la dimensione massima del buffer e stdin è il puntatore a stdin. Ad esempio, per leggere una stringa di input dall'utente e memorizzarla in una variabile str, utilizziamo la seguente istruzione:  
   
```  
fgets(str, 100, stdin);  
```  
   
Dove 100 è la dimensione massima del buffer.  
   
Evitare problemi di sicurezza con fgets()  
La funzione scanf() può essere pericolosa perché non verifica la dimensione del buffer in cui memorizzare l'input dell'utente. Questo può portare a problemi di sicurezza come buffer overflow. Per evitare questo tipo di problema, è consigliabile utilizzare la funzione fgets() e verificare sempre la dimensione del buffer. Ad esempio, la seguente istruzione utilizza fgets() per leggere una stringa di input dell'utente e verificare la dimensione del buffer:  
   
```  
fgets(str, sizeof(str), stdin);  
```  
   
Dove sizeof(str) restituisce la dimensione del buffer str.  


## Esempio 1a: inserire un numero positivo (WHILE)

Ecco un esempio di programma in cui l'utente deve inserire un numero positivo e il programma stampa il numero a schermo. Se l'utente inserisce un numero negativo o zero, il programma richiede di inserire un altro numero.  
   
```  
#include <stdio.h>  
   
int main() {  
    int num;  
    printf("Inserisci un numero positivo: ");  
    scanf("%d", &num);  
    while(num <= 0) {  
        printf("Il numero inserito non è positivo. Inserisci un altro numero: ");  
        scanf("%d", &num);  
    }  
    printf("Il numero inserito è: %d", num);  
    return 0;  
}  
```  
   
In questo esempio, la funzione scanf() viene utilizzata per leggere il numero inserito dall'utente e assegnarlo alla variabile num. Se il numero inserito è negativo o zero, il programma entra in un ciclo while che richiede all'utente di inserire un altro numero. Il ciclo si ripete finché l'utente non inserisce un numero positivo. Infine, il programma stampa il numero inserito a schermo utilizzando la funzione printf().

## Esempio 2a: inserire un numero positivo (DO-WHILE)

Ecco un altro esempio di programma in cui l'utente deve inserire un numero positivo e il programma stampa il numero a schermo. Questa volta verrà utilizzato il ciclo do while.  
   
```  
#include <stdio.h>  
   
int main() {  
    int num;  
    do {  
        printf("Inserisci un numero positivo: ");  
        scanf("%d", &num);  
    } while(num <= 0);  
    printf("Il numero inserito è: %d", num);  
    return 0;  
}  
```

## Lettura input con fget

Per leggere un numero positivo utilizzando la funzione fgets(), dobbiamo prima leggere l'input dell'utente come una stringa di caratteri utilizzando la funzione fgets(), quindi convertire la stringa in un numero utilizzando la funzione strtol().  
   
Ecco un esempio di programma in cui viene utilizzata la funzione fgets() per leggere un numero positivo dall'utente:  
   
```  
#include <stdio.h>  
#include <stdlib.h>  
#include <string.h>  
   
int main() {  
    char str[100];  
    int num;  
    char *endptr;  
    printf("Inserisci un numero positivo: ");  
    fgets(str, sizeof(str), stdin);  
    str[strcspn(str, "\n")] = '\0'; // Rimuove il carattere di newline dalla stringa  
    num = strtol(str, &endptr, 10);  
    if(num <= 0 || *endptr != '\0') {  
        printf("Il numero inserito non è positivo. Riprova.\n");  
        return 1;  
    }  
    printf("Il numero inserito è: %d\n", num);  
    return 0;  
}  
```  
   
In questo esempio, viene utilizzata la funzione fgets() per leggere l'input dell'utente come una stringa di caratteri. La funzione strcspn() viene utilizzata per rimuovere il carattere di newline dalla stringa. Successivamente, viene utilizzata la funzione strtol() per convertire la stringa in un numero intero. La variabile endptr viene utilizzata per verificare se la conversione è stata effettuata correttamente. Se il numero letto non è positivo o se la conversione non è stata effettuata correttamente, viene stampato un messaggio di errore. Altrimenti, il programma stampa il numero inserito a schermo utilizzando la funzione printf().
   
