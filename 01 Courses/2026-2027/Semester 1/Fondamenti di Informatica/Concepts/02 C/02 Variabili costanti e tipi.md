---
course: Fondamenti di Informatica
type: concept
topic: Variabili, costanti e tipi in C
status: draft
---

# Variabili, costanti e tipi

## Variabili

Una variabile è uno spazio di memoria identificato da un nome, nel quale il programma conserva un valore. Il tipo stabilisce come quel valore viene rappresentato e quali operazioni sono ammesse.

```c
int eta = 20;
```

In questa dichiarazione:

- `int` è il tipo;
- `eta` è il nome della variabile;
- `20` è il valore iniziale;
- `=` è l'operatore di assegnazione.

Il valore può essere modificato in seguito:

```c
eta = 21;
```

Una variabile locale non inizializzata non contiene automaticamente zero. Leggerla prima di averle assegnato un valore produce un comportamento indefinito.

```c
int numero;      // dichiarata, ma non ancora inizializzata
numero = 10;     // ora contiene un valore valido
```

## Costanti

Una costante letterale è un valore scritto direttamente nel codice, come `10`, `3.14` o `'A'`.

Quando un valore non deve cambiare, si può dichiarare un oggetto con `const`:

```c
const double PI = 3.1415926535;
```

Un'assegnazione successiva non è ammessa:

```c
PI = 3.0;  // errore
```

Usare un nome come `PI` rende il significato più chiaro ed evita di ripetere nel programma un valore scritto “a mano”.

## Tipi fondamentali

| Tipo | Esempi | Uso tipico |
| --- | --- | --- |
| `int` | `3`, `-10`, `100` | numeri interi |
| `float` | `12.5f` | numeri reali con precisione singola |
| `double` | `3.1415926535` | numeri reali con precisione maggiore |
| `char` | `'A'`, `'7'` | un singolo carattere |

Esempio:

```c
int eta = 20;
float prezzo = 12.5f;
double pi = 3.1415926535;
char lettera = 'A';
```

Le dimensioni esatte dei tipi dipendono dall'implementazione. L'operatore `sizeof` permette di misurarle:

```c
printf("%zu\n", sizeof(int));
```

## Caratteri e stringhe

Un carattere usa gli apici singoli:

```c
char lettera = 'A';
```

Una sequenza di caratteri usa le virgolette doppie e, in C, viene memorizzata in un array di `char` terminato dal carattere speciale `\0`:

```c
char nome[] = "Mario";
```

Le stringhe verranno approfondite insieme agli array. Qui è importante non confondere `'A'` con `"A"`.

## Errori comuni

- usare una variabile locale prima di inizializzarla;
- mettere una stringa tra apici singoli o un carattere tra virgolette doppie;
- dimenticare il suffisso `f` quando si vuole indicare esplicitamente un letterale `float`;
- pensare che `const` sia una variabile da modificare durante l'esecuzione.

## Collegamenti

- [[03 Input e output con printf e scanf|Input e output con `printf` e `scanf`]]
- [[04 Operatori e cast|Operatori e cast]]
