---
course: Fondamenti di Informatica
type: concept
topic: Condizioni e costrutto if
status: draft
---

# Condizioni e costrutto `if`

## Perché serve

`if` permette al programma di scegliere quali istruzioni eseguire in base al valore di una condizione.

```c
int eta = 20;

if (eta >= 18) {
    printf("Sei maggiorenne\n");
}
```

La struttura generale è:

```c
if (condizione) {
    // eseguito soltanto se la condizione è vera
}
```

## `if` e `else`

`else` introduce il ramo eseguito quando la condizione è falsa:

```c
if (eta >= 18) {
    printf("Sei maggiorenne\n");
} else {
    printf("Sei minorenne\n");
}
```

Viene eseguito esattamente uno dei due rami.

## Catena `else if`

```c
if (voto >= 8) {
    printf("Ottimo\n");
} else if (voto >= 6) {
    printf("Sufficiente\n");
} else {
    printf("Insufficiente\n");
}
```

Le condizioni vengono controllate dall'alto verso il basso. Appena una è vera, viene eseguito il relativo blocco e il resto della catena viene saltato. Per questo l'ordine conta: con `voto = 9`, la prima condizione vera deve essere `voto >= 8`, non `voto >= 6`.

## Operatori di confronto

| Operatore | Significato | Esempio |
| --- | --- | --- |
| `==` | uguale | `x == 5` |
| `!=` | diverso | `x != 5` |
| `>` | maggiore | `x > 5` |
| `<` | minore | `x < 5` |
| `>=` | maggiore o uguale | `x >= 5` |
| `<=` | minore o uguale | `x <= 5` |

`=` e `==` hanno ruoli diversi:

```c
x = 5;   // assegna 5 a x
x == 5;  // verifica se x è uguale a 5
```

## Operatori logici

| Operatore | Significato | Quando è vero |
| --- | --- | --- |
| `&&` | AND | entrambe le condizioni sono vere |
| `||` | OR | almeno una condizione è vera |
| `!` | NOT | la condizione originale è falsa |

```c
if (eta >= 18 && eta <= 30) {
    printf("Hai tra 18 e 30 anni\n");
}

if (numero == 1 || numero == 2) {
    printf("Hai inserito 1 oppure 2\n");
}

if (!(numero == 5)) {
    printf("Il numero non e 5\n");
}
```

L'ultima condizione si può scrivere più chiaramente come `numero != 5`.

Gli operatori `&&` e `||` usano la valutazione a corto circuito: C evita di valutare la seconda condizione quando il risultato è già determinato dalla prima.

## Vero e falso in C

In una condizione numerica:

- `0` significa falso;
- qualsiasi valore diverso da `0` significa vero.

```c
int x = 5;

if (x) {
    printf("Vero\n");
}
```

Il blocco viene eseguito perché `x` è diverso da zero.

## Esempio: positivo, negativo o zero

```c
if (numero > 0) {
    printf("Positivo\n");
} else if (numero < 0) {
    printf("Negativo\n");
} else {
    printf("Zero\n");
}
```

I tre casi sono mutuamente esclusivi e coprono tutti i valori interi possibili.

## Errori comuni

- usare `=` invece di `==` in una condizione;
- scrivere una catena di soglie nell'ordine sbagliato;
- dimenticare le parentesi attorno alla condizione;
- usare `&` e `|` al posto di `&&` e `||`;
- credere che soltanto `1` sia vero: in C è vero ogni valore diverso da zero;
- non usare le graffe e rendere ambiguo quale istruzione appartenga all'`if`.

## Collegamenti

- [[03 Input e output con printf e scanf|Input e output con `printf` e `scanf`]]
- [[06 Esempio completo|Esempio completo]]
