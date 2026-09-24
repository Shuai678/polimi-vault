---
course: Fondamenti di Informatica
type: concept
topic: Operatori aritmetici e cast
status: draft
---

# Operatori e cast

## Operatori aritmetici

| Operatore | Significato | Esempio |
| --- | --- | --- |
| `+` | somma | `a + b` |
| `-` | sottrazione | `a - b` |
| `*` | moltiplicazione | `a * b` |
| `/` | divisione | `a / b` |
| `%` | resto della divisione intera | `a % b` |

```c
int a = 10;
int b = 3;

int somma = a + b;        // 13
int differenza = a - b;   // 7
int prodotto = a * b;     // 30
int quoziente = a / b;    // 3
int resto = a % b;        // 1
```

## Divisione intera

Se entrambi gli operandi sono interi, anche la divisione è intera:

```c
int a = 10;
int b = 3;

printf("%d\n", a / b);  // stampa 3
```

La parte frazionaria viene scartata. Non si ottiene `3.333333`.

## Cast esplicito

Un cast chiede di convertire esplicitamente un valore in un altro tipo. La sintassi è:

```c
(tipo) espressione
```

Per ottenere una divisione reale è sufficiente rendere reale almeno uno dei due operandi:

```c
float risultato = (float)a / b;
printf("%f\n", risultato);  // circa 3.333333
```

Il cast viene applicato ad `a` prima della divisione. A quel punto C converte anche `b` e svolge una divisione in virgola mobile.

Queste due espressioni non sono equivalenti:

```c
(float)(a / b)  // prima calcola 10 / 3 = 3, poi converte 3 in 3.0
(float)a / b    // converte a, poi calcola la divisione reale
```

## Conversione da reale a intero

```c
float x = 5.8f;
int y = (int)x;

printf("%d\n", y);  // stampa 5
```

Il cast a `int` non arrotonda: elimina la parte frazionaria, troncando verso zero.

## Conversioni implicite

C può eseguire alcune conversioni automaticamente:

```c
int n = 5;
double risultato = n + 0.5;
```

In questa espressione `n` viene convertito in `double`. È comunque importante capire quali tipi partecipano all'operazione, perché una conversione eseguita troppo tardi non recupera informazioni già perse.

## Errori comuni

- aspettarsi un risultato decimale da `int / int`;
- scrivere `(float)(a / b)` pensando di rendere reale la divisione;
- credere che il cast da `float` a `int` arrotondi;
- usare `%` con operandi in virgola mobile;
- dividere per zero.

## Collegamenti

- [[02 Variabili costanti e tipi|Variabili, costanti e tipi]]
- [[05 Condizioni e costrutto if|Condizioni e costrutto `if`]]
