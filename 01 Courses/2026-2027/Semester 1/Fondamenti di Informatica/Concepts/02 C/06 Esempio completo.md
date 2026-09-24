---
course: Fondamenti di Informatica
type: worked-example
topic: Media di due voti in C
status: draft
---

# Esempio completo

## Problema

Leggere due voti interi, calcolarne la media e stabilire se lo studente è promosso. La soglia di sufficienza è `6`.

## Codice

```c
#include <stdio.h>

int main(void) {
    int voto1;
    int voto2;

    printf("Inserisci il primo voto: ");
    if (scanf("%d", &voto1) != 1) {
        printf("Input non valido\n");
        return 1;
    }

    printf("Inserisci il secondo voto: ");
    if (scanf("%d", &voto2) != 1) {
        printf("Input non valido\n");
        return 1;
    }

    float media = (float)(voto1 + voto2) / 2;

    printf("La media e: %.2f\n", media);

    if (media >= 6) {
        printf("Promosso\n");
    } else {
        printf("Non promosso\n");
    }

    return 0;
}
```

## Traccia con input `7` e `8`

1. `voto1` riceve `7`.
2. `voto2` riceve `8`.
3. `voto1 + voto2` produce `15`.
4. Il cast trasforma `15` in `15.0f` prima della divisione.
5. `15.0f / 2` produce `7.5f`.
6. `media >= 6` è vera.
7. Il programma stampa:

```text
La media e: 7.50
Promosso
```

## Perché il cast è necessario

Senza cast:

```c
float media = (voto1 + voto2) / 2;
```

con somma `15`, l'espressione a destra eseguirebbe prima la divisione intera `15 / 2`, ottenendo `7`; soltanto dopo il valore verrebbe convertito in `7.0f`.

## Schema mentale

```text
variabili → input → elaborazione → condizione → output
```

Questo esempio collega:

- [[01 Struttura di un programma C|la struttura del programma]];
- [[02 Variabili costanti e tipi|variabili e tipi]];
- [[03 Input e output con printf e scanf|`scanf` e `printf`]];
- [[04 Operatori e cast|operatori e cast]];
- [[05 Condizioni e costrutto if|condizioni e `if`]].
