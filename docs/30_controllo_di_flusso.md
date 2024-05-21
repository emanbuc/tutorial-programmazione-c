# Tutorial sulle Strutture di Controllo di Flusso in C

Le strutture di controllo di flusso in C sono fondamentali per dirigere l'esecuzione del programma. In questo tutorial, esploreremo le principali strutture di controllo: `if`, `else`, `else if`, `switch`, i cicli `for`, `while` e `do-while`, e le istruzioni di salto `break` e `continue`.

## Struttura Condizionale: `if`, `else`, `else if`

### `if`
La struttura `if` permette di eseguire un blocco di codice solo se una condizione è vera.

```c
#include <stdio.h>

int main() {
    int x = 10;

    if (x > 0) {
        printf("x è positivo\n");
    }

    return 0;
}
```

### `else`
La struttura `else` viene utilizzata insieme a `if` per eseguire un blocco di codice quando la condizione `if` è falsa.

```c
#include <stdio.h>

int main() {
    int x = -5;

    if (x > 0) {
        printf("x è positivo\n");
    } else {
        printf("x non è positivo\n");
    }

    return 0;
}
```

### `else if`
La struttura `else if` permette di verificare ulteriori condizioni se le precedenti sono false.

```c
#include <stdio.h>

int main() {
    int x = 0;

    if (x > 0) {
        printf("x è positivo\n");
    } else if (x < 0) {
        printf("x è negativo\n");
    } else {
        printf("x è zero\n");
    }

    return 0;
}
```

## Struttura Condizionale: `switch`

La struttura `switch` valuta un'espressione e esegue il blocco di codice associato al caso corrispondente.

```c
#include <stdio.h>

int main() {
    int day = 3;

    switch (day) {
        case 1:
            printf("Lunedì\n");
            break;
        case 2:
            printf("Martedì\n");
            break;
        case 3:
            printf("Mercoledì\n");
            break;
        default:
            printf("Giorno non valido\n");
            break;
    }

    return 0;
}
```

## Ciclo `for`

Il ciclo `for` è utilizzato per eseguire un blocco di codice un numero specifico di volte.

```c
#include <stdio.h>

int main() {
    for (int i = 0; i < 5; i++) {
        printf("i = %d\n", i);
    }

    return 0;
}
```

## Ciclo `while`

Il ciclo `while` continua a eseguire il blocco di codice fintanto che la condizione è vera.

```c
#include <stdio.h>

int main() {
    int i = 0;

    while (i < 5) {
        printf("i = %d\n", i);
        i++;
    }

    return 0;
}
```

## Ciclo `do-while`

Il ciclo `do-while` è simile al `while`, ma verifica la condizione dopo aver eseguito il blocco di codice almeno una volta.

```c
#include <stdio.h>

int main() {
    int i = 0;

    do {
        printf("i = %d\n", i);
        i++;
    } while (i < 5);

    return 0;
}
```

## Istruzioni di salto: `break` e `continue`

### `break`
L'istruzione `break` termina l'esecuzione del ciclo corrente.

```c
#include <stdio.h>

int main() {
    for (int i = 0; i < 10; i++) {
        if (i == 5) {
            break;
        }
        printf("i = %d\n", i);
    }

    return 0;
}
```

### `continue`
L'istruzione `continue` salta l'iterazione corrente del ciclo e passa alla successiva.

```c
#include <stdio.h>

int main() {
    for (int i = 0; i < 10; i++) {
        if (i % 2 == 0) {
            continue;
        }
        printf("i = %d\n", i);
    }

    return 0;
}
```

## Conclusione

Le strutture di controllo di flusso sono essenziali per dirigere l'esecuzione del codice in base alle condizioni e ai requisiti specifici del programma. Comprendere come utilizzare `if`, `else`, `else if`, `switch`, i cicli `for`, `while`, `do-while`, e le istruzioni `break` e `continue` è fondamentale per scrivere codice C efficace e robusto.
