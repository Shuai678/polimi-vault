---
course: Fondamenti di Informatica
type: concept
topic: printf e scanf
status: draft
---

# Input e output con `printf` e `scanf`

Le funzioni `printf` e `scanf` sono dichiarate in `<stdio.h>`:

```c
#include <stdio.h>
```

## Output con `printf`

`printf` mostra testo e valori sul terminale.

```c
printf("Ciao!\n");
```

Per inserire il valore di una variabile nell'output si usano specificatori di conversione:

| Tipo del valore | Specificatore di `printf` |
| --- | --- |
| `int` | `%d` |
| `float` o `double` | `%f` |
| `char` | `%c` |
| stringa | `%s` |

```c
int eta = 20;
double altezza = 1.75;
char voto = 'A';

printf("Eta: %d\n", eta);
printf("Altezza: %.2f\n", altezza);
printf("Voto: %c\n", voto);
```

In `%.2f`, `.2` richiede due cifre dopo il punto decimale.

## Input con `scanf`

`scanf` legge dati formattati dall'input standard e li scrive nelle variabili indicate.

```c
int eta;

printf("Inserisci la tua eta: ");
scanf("%d", &eta);
printf("Hai %d anni.\n", eta);
```

Nell'istruzione

```c
scanf("%d", &eta);
```

- `%d` indica che ci si aspetta un intero;
- `&eta` fornisce l'indirizzo di memoria nel quale `scanf` deve salvare il valore.

## Specificatori principali

| Tipo della variabile | `printf` | `scanf` |
| --- | --- | --- |
| `int` | `%d` | `%d` |
| `float` | `%f` | `%f` |
| `double` | `%f` | `%lf` |
| `char` | `%c` | `%c` |
| stringa | `%s` | `%s` |

La differenza per `double` è importante: con `scanf` si usa `%lf`, mentre con `printf` si usa `%f`.

```c
int numero;
float prezzo;
double altezza;
char lettera;

scanf("%d", &numero);
scanf("%f", &prezzo);
scanf("%lf", &altezza);
scanf(" %c", &lettera);
```

Lo spazio prima di `%c` fa consumare eventuali spazi o `\n` rimasti nell'input.

## Controllare che la lettura sia riuscita

`scanf` restituisce il numero di valori letti correttamente. Un controllo semplice è:

```c
int numero;

if (scanf("%d", &numero) != 1) {
    printf("Input non valido\n");
    return 1;
}
```

Senza controllo, se l'utente inserisce un dato del tipo sbagliato, la variabile potrebbe non ricevere un valore valido.

## Nota introduttiva sulle stringhe

```c
char nome[50];
scanf("%49s", nome);
```

Qui non si scrive `&nome`. Il limite `49` lascia spazio al carattere finale `\0` e protegge la dimensione dell'array. `%s` si ferma però al primo spazio: inserendo `Mario Rossi` viene letto soltanto `Mario`. Per leggere un'intera riga si usa normalmente `fgets`.

## Errori comuni

- scrivere `prints` invece di `printf`;
- usare uno specificatore non coerente con il tipo della variabile;
- dimenticare `&` negli argomenti numerici e `char` di `scanf`;
- usare `%f` al posto di `%lf` per leggere un `double`;
- dimenticare lo spazio in `" %c"` dopo una lettura precedente;
- assumere che `scanf` abbia sempre letto correttamente.

## Collegamenti

- [[01 Struttura di un programma C|Struttura di un programma C]]
- [[02 Variabili costanti e tipi|Variabili, costanti e tipi]]
- [[06 Esempio completo|Esempio completo]]
