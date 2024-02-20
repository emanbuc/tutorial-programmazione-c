# Introduzione al Linguaggio C

Il linguaggio di programmazione C è un potente strumento utilizzato per lo sviluppo di software in vari contesti, dai sistemi operativi ai dispositivi embedded. È noto per la sua efficienza, la sua portabilità e la sua capacità di lavorare a basso livello, ma offre anche un'elevata flessibilità per lo sviluppo di applicazioni di alto livello. In questa lezione, esploreremo i fondamenti del linguaggio C, dalla sintassi di base alle strutture dati più comuni.
I vari elementi del linguaggio saranno poi approfonditi nelle lezioni successive.

## Primi Passi

### Ambiente di sviluppo

Per iniziare a scrivere programmi in C, hai bisogno di un editor e di un compilatore C installato sul tuo sistema. 
Alcuni compilatori C popolari includono GCC (GNU Compiler Collection) e Clang. Una volta installato il compilatore, puoi creare e compilare il tuo primo programma C. 
In ambiente Widows è popolare l'utilizzo Visual C++, incluso nelle versioni recenti di Visual Studio tuttavia negli esempi che seguono si farà riferimento al compilatore GCC che si trova comunemente già pre-installato in MacOS e Linux.

Su widows un modo semplice di utilizzare GCC è [installare il supporto C/C++ in Visual Studio Code](https://code.visualstudio.com/docs/cpp/config-mingw) attraverso mingw64.
Gli esempi proposti dovrebbero funzionare anche utilizzando Visual Studio.

### Hello World

Ecco un esempio di programma "Hello, World!":

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

Nel codice sopra, `#include <stdio.h>` è una direttiva di pre-processore che include il file di intestazione `stdio.h`, che contiene le definizioni di funzioni di input/output standard come `printf`. La funzione `printf` è utilizzata per stampare il testo sulla console.

## Compilazione e Esecuzione

Per compilare il programma C, salvalo con un'estensione ".c", ad esempio "hello.c". Quindi, apri il terminale e digita il comando seguente:

```
gcc hello.c -o hello
```

Questo comando utilizza il compilatore GCC per compilare il file "hello.c" e produce un file eseguibile chiamato "hello". Per eseguire il programma, digita il seguente comando:

```
./hello
```

## Variabili e Tipi di Dati

In C, puoi dichiarare variabili di diversi tipi di dati, come `int`, `float`, `char`, etc. Ad esempio:

```c
int age = 25;
float height = 5.9;
char grade = 'A';
```

### Strutture di Controllo

Le strutture di controllo, come `if`, `else`, `for`, `while`, etc., consentono di controllare il flusso di esecuzione del programma. Ecco un esempio di utilizzo di `if` e `else`:

```c
int number = 10;
if (number > 0) {
    printf("Il numero è positivo\n");
} else {
    printf("Il numero è negativo\n");
}
```

## Funzioni

Le funzioni consentono di suddividere il codice in blocchi più piccoli e riutilizzabili. Ad esempio:

```c
int somma(int a, int b) {
    return a + b;
}

int main() {
    int risultato = somma(3, 5);
    printf("La somma è: %d\n", risultato);
    return 0;
}
```
