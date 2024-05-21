# Tutorial sulle Strutture di Controllo di Flusso in C++

Le strutture di controllo di flusso in C++ sono fondamentali per dirigere l'esecuzione del programma. In questo tutorial, esploreremo le principali strutture di controllo: `if`, `else`, `else if`, `switch`, i cicli `for`, `while` e `do-while`, e le istruzioni di salto `break` e `continue`.

## Struttura Condizionale: `if`, `else`, `else if`

### `if`
La struttura `if` permette di eseguire un blocco di codice solo se una condizione è vera.

```cpp
int x = 10;

if (x > 0) {
    std::cout << "x è positivo" << std::endl;
}
```

### `else`
La struttura `else` viene utilizzata insieme a `if` per eseguire un blocco di codice quando la condizione `if` è falsa.

```cpp
int x = -5;

if (x > 0) {
    std::cout << "x è positivo" << std::endl;
} else {
    std::cout << "x non è positivo" << std::endl;
}
```

### `else if`
La struttura `else if` permette di verificare ulteriori condizioni se le precedenti sono false.

```cpp
int x = 0;

if (x > 0) {
    std::cout << "x è positivo" << std::endl;
} else if (x < 0) {
    std::cout << "x è negativo" << std::endl;
} else {
    std::cout << "x è zero" << std::endl;
}
```

## Struttura Condizionale: `switch`

La struttura `switch` valuta un'espressione e esegue il blocco di codice associato al caso corrispondente.

```cpp
int day = 3;

switch (day) {
    case 1:
        std::cout << "Lunedì" << std::endl;
        break;
    case 2:
        std::cout << "Martedì" << std::endl;
        break;
    case 3:
        std::cout << "Mercoledì" << std::endl;
        break;
    default:
        std::cout << "Giorno non valido" << std::endl;
        break;
}
```

## Ciclo `for`

Il ciclo `for` è utilizzato per eseguire un blocco di codice un numero specifico di volte.

```cpp
for (int i = 0; i < 5; i++) {
    std::cout << "i = " << i << std::endl;
}
```

## Ciclo `while`

Il ciclo `while` continua a eseguire il blocco di codice fintanto che la condizione è vera.

```cpp
int i = 0;

while (i < 5) {
    std::cout << "i = " << i << std::endl;
    i++;
}
```

## Ciclo `do-while`

Il ciclo `do-while` è simile al `while`, ma verifica la condizione dopo aver eseguito il blocco di codice almeno una volta.

```cpp
int i = 0;

do {
    std::cout << "i = " << i << std::endl;
    i++;
} while (i < 5);
```

## Istruzioni di salto: `break` e `continue`

### `break`
L'istruzione `break` termina l'esecuzione del ciclo corrente.

```cpp
for (int i = 0; i < 10; i++) {
    if (i == 5) {
        break;
    }
    std::cout << "i = " << i << std::endl;
}
```

### `continue`
L'istruzione `continue` salta l'iterazione corrente del ciclo e passa alla successiva.

```cpp
for (int i = 0; i < 10; i++) {
    if (i % 2 == 0) {
        continue;
    }
    std::cout << "i = " << i << std::endl;
}
```

## Conclusione

Le strutture di controllo di flusso sono essenziali per dirigere l'esecuzione del codice in base alle condizioni e ai requisiti specifici del programma. Comprendere come utilizzare `if`, `else`, `else if`, `switch`, i cicli `for`, `while`, `do-while`, e le istruzioni `break` e `continue` è fondamentale per scrivere codice C++ efficace e robusto.
