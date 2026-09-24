---
course: Fondamenti di Informatica
type: concept
topic: Struttura di un programma C
status: draft
---

# Struttura di un programma C

## Struttura generale

Nel modello introduttivo usato nel corso, un programma C può essere suddiviso in:

1. **direttive del preprocessore**;
2. **parte dichiarativa globale**;
3. **funzione `main`**, composta da:
   1. parte dichiarativa locale;
   2. parte esecutiva.

> [!important]
> Il termine corretto è **preprocessore**, non “processore”. Il preprocessore interviene sul testo del programma prima della compilazione vera e propria.

```c
// 1. Direttive del preprocessore
#include <stdio.h>
#define SOGLIA 18

// 2. Parte dichiarativa globale
const char MESSAGGIO[] = "Controllo eta";
int numero_controlli = 0;
int e_maggiorenne(int eta);       // prototipo di funzione

// 3. Funzione main
int main(void) {
    // 3.1 Parte dichiarativa locale
    int eta;

    // 3.2 Parte esecutiva
    printf("%s\n", MESSAGGIO);
    printf("Inserisci la tua eta: ");

    if (scanf("%d", &eta) != 1) {
        printf("Input non valido\n");
        return 1;
    }

    numero_controlli = numero_controlli + 1;

    if (e_maggiorenne(eta)) {
        printf("Sei maggiorenne\n");
    } else {
        printf("Sei minorenne\n");
    }

    return 0;
}

// Definizione di una funzione diversa da main
int e_maggiorenne(int eta) {
    return eta >= SOGLIA;
}
```

Questa divisione aiuta a riconoscere le parti del programma; non significa che ogni programma debba contenere tutti questi elementi.

### 1. Direttive del preprocessore

Le direttive iniziano con `#` e vengono elaborate prima della compilazione.

```c
#include <stdio.h>
#define SOGLIA 18
```

- `#include` inserisce le dichiarazioni contenute in un file di intestazione;
- `#define` definisce una macro testuale.

Le direttive del preprocessore non sono normali istruzioni C e normalmente non terminano con `;`.

### 2. Parte dichiarativa globale

Si trova fuori da tutte le funzioni e può contenere, per esempio:

- costanti e variabili globali;
- prototipi di funzione;
- definizioni di tipi;
- definizioni di funzioni.

```c
const double PI = 3.1415926535;
int quadrato(int numero);
```

Gli elementi globali possono essere visibili a più funzioni. Le variabili globali vanno usate con cautela, perché rendono più difficile capire quali parti del programma ne modificano il valore.

### 3. Funzione `main`

`main` è il punto dal quale comincia l'esecuzione del programma.

```c
int main(void) {
    return 0;
}
```

#### 3.1 Parte dichiarativa locale

Contiene le variabili dichiarate all'interno di `main`. Queste variabili sono locali alla funzione e possono essere usate soltanto nel loro ambito.

```c
int numero;
double media;
```

Nel C moderno, a partire da C99, le dichiarazioni possono anche essere mescolate alle istruzioni eseguibili. La separazione tra parte dichiarativa e parte esecutiva rimane comunque un buon modello iniziale per leggere la struttura del programma.

#### 3.2 Parte esecutiva

Contiene le istruzioni che realizzano l'algoritmo: input, assegnazioni, calcoli, chiamate di funzione, condizioni e output.

```c
scanf("%d", &numero);
media = numero / 2.0;

if (media >= 6) {
    printf("Sufficiente\n");
}
```

## Programma minimo

```c
#include <stdio.h>

int main(void) {
    printf("Ciao!\n");
    return 0;
}
```

## Come si legge

### `#include <stdio.h>`

Rende disponibili le dichiarazioni delle funzioni di input e output della libreria standard, tra cui `printf` e `scanf`.

### `int main(void)`

`main` è la funzione dalla quale inizia l'esecuzione del programma.

- `int` indica che la funzione restituisce un numero intero al sistema operativo;
- `void` indica che, in questo caso, non riceve argomenti;
- le parentesi graffe `{` e `}` delimitano il corpo della funzione.

### Le istruzioni

```c
printf("Ciao!\n");
return 0;
```

Le istruzioni terminano normalmente con `;`. `printf` produce un output; `return 0` segnala che il programma è terminato correttamente.

La sequenza `\n` inserita nella stringa manda il cursore a capo.

## Commenti

I commenti servono a spiegare il codice e vengono ignorati durante l'esecuzione.

```c
// Commento su una riga

/* Commento
   su più righe */
```

## Ordine di esecuzione

All'interno di `main`, le istruzioni vengono normalmente eseguite dall'alto verso il basso. I costrutti di controllo, come [[05 Condizioni e costrutto if|`if`]], possono cambiare quali istruzioni vengono eseguite.

## Errori comuni

- dimenticare `#include <stdio.h>` quando si usano `printf` o `scanf`;
- dimenticare il `;` alla fine di un'istruzione;
- non chiudere una parentesi o una graffa;
- scrivere codice eseguibile fuori da una funzione;
- confondere `\n` con il carattere `/n`.

## Collegamenti

- [[00A Linguaggi di programmazione e storia del C|Linguaggi di programmazione e storia del C]]
- [[02 Variabili costanti e tipi|Variabili, costanti e tipi]]
- [[03 Input e output con printf e scanf|Input e output con `printf` e `scanf`]]
