---
course: Fondamenti di Informatica
type: concept
topic: Linguaggi di programmazione e storia del C
status: draft
---

# Linguaggi di programmazione e storia del C

## Il linguaggio di programmazione è un linguaggio formale

Un linguaggio di programmazione è un **linguaggio formale**: i programmi devono rispettare regole precise, definite dal linguaggio. Non funziona come una lingua naturale, nella quale una frase può essere ambigua o interpretata dal contesto.

Le due idee fondamentali sono **sintassi** e **semantica**.

### Sintassi: come deve essere scritto il programma

La sintassi è l'insieme delle regole che stabiliscono quali sequenze di simboli formano un programma valido. Riguarda quindi la **forma** del codice.

```c
int x = 5;
```

Questa istruzione rispetta la sintassi del C. Invece:

```c
int x = ;
```

non è sintatticamente corretta, perché dopo `=` manca l'espressione che deve fornire il valore.

Elementi sintattici del C sono, per esempio:

- parole chiave come `int`, `if` e `return`;
- identificatori come `x` e `numero`;
- operatori come `+`, `=` e `>=`;
- segni di punteggiatura come `;`, `(`, `)` e `{ }`;
- regole che indicano in quale ordine questi elementi possono apparire.

Il compilatore segnala normalmente una violazione della sintassi e non riesce a tradurre il programma.

### Semantica: che cosa significa il programma

La semantica stabilisce il **significato** delle costruzioni sintatticamente valide, cioè quale comportamento producono.

```c
int x = 2 + 3;
```

La sintassi dice che questa è una dichiarazione valida. La semantica stabilisce che prima si calcola `2 + 3` e poi si inizializza `x` con il valore `5`.

Due istruzioni possono essere entrambe sintatticamente valide ma avere significati diversi:

```c
x = 5;   // assegna 5 a x
x == 5;  // confronta x con 5
```

Un programma può quindi rispettare la sintassi ma non fare ciò che il programmatore desiderava: in quel caso il problema non è grammaticale, ma logico o semantico.

### Schema da ricordare

| Domanda | Concetto |
| --- | --- |
| «È scritto secondo le regole del linguaggio?» | sintassi |
| «Che cosa significa e che effetto produce?» | semantica |

## Linguaggi di alto e basso livello

Il “livello” descrive quanto il linguaggio è vicino all'hardware oppure al modo in cui le persone esprimono algoritmi. Non esiste un confine assoluto: è soprattutto un confronto tra linguaggi e livelli di astrazione.

### Basso livello

Un linguaggio di basso livello espone direttamente molti dettagli della macchina ed è legato a una specifica architettura.

- Il **linguaggio macchina** è formato dalle istruzioni binarie eseguite direttamente dal processore.
- Il **linguaggio assembly** usa nomi simbolici per istruzioni molto vicine a quelle della CPU.

Esempio indicativo di assembly x86-64:

```asm
mov eax, 5
add eax, 3
```

Vantaggi tipici:

- controllo molto diretto dell'hardware;
- possibilità di ottimizzare casi estremamente specifici.

Svantaggi tipici:

- codice più difficile da scrivere e mantenere;
- forte dipendenza dall'architettura del processore;
- minore portabilità.

### Alto livello

Un linguaggio di alto livello permette di esprimere algoritmi usando astrazioni come variabili, espressioni, funzioni e strutture di controllo, nascondendo molti dettagli della macchina.

```c
int risultato = 5 + 3;
```

Esempi comuni sono C, Python e Java, anche se offrono livelli di astrazione diversi.

Vantaggi tipici:

- maggiore leggibilità;
- sviluppo e manutenzione più semplici;
- migliore portabilità tra macchine diverse.

### Dove si colloca il C?

Il C è un linguaggio di **alto livello** rispetto al linguaggio macchina e all'assembly, perché consente di scrivere algoritmi con variabili, funzioni e strutture di controllo indipendenti da una singola CPU.

Allo stesso tempo rimane vicino alla macchina: permette di lavorare con indirizzi, puntatori, bit e memoria con poche astrazioni obbligatorie. Per questo viene talvolta chiamato informalmente linguaggio di “medio livello”, ma questa non è una categoria formale.

## Linguaggi compilati e interpretati

La distinzione riguarda il modo in cui un'implementazione esegue il codice. Non è sempre una proprietà assoluta del linguaggio: lo stesso linguaggio può avere implementazioni diverse o combinare più tecniche.

### Compilazione

Un compilatore traduce il codice sorgente in un'altra forma, spesso codice macchina, **prima** dell'esecuzione.

```text
codice sorgente → compilatore → programma eseguibile → esecuzione
```

Il C viene normalmente compilato. In forma semplificata, la costruzione di un programma C comprende:

1. **preprocessamento**: elabora le direttive che iniziano con `#`;
2. **compilazione**: traduce il C e controlla le regole del linguaggio;
3. **assemblaggio**: produce codice oggetto;
4. **collegamento o linking**: unisce codice oggetto e librerie nell'eseguibile.

Esempi tipicamente compilati in codice macchina: C, C++, Rust.

### Interpretazione

Un interprete esegue il programma attraverso un altro programma, traducendo o analizzando le istruzioni durante l'esecuzione.

```text
codice sorgente → interprete → esecuzione
```

Python è spesso chiamato linguaggio interpretato. Più precisamente, l'implementazione CPython compila normalmente il sorgente in **bytecode**, che viene poi eseguito dalla macchina virtuale di Python.

### Soluzioni ibride

Molte implementazioni moderne combinano compilazione e interpretazione:

- Java compila il sorgente in bytecode per la JVM;
- la JVM può interpretare il bytecode e compilare durante l'esecuzione le parti più usate tramite JIT;
- i motori JavaScript moderni usano normalmente interpretazione e compilazione JIT.

Quindi è più preciso dire che **un'implementazione** usa una certa strategia, invece di dividere rigidamente tutti i linguaggi in due gruppi.

## Breve storia del C

- Tra il **1969 e il 1973**, ai Bell Labs, **Dennis Ritchie** sviluppò il C durante la nascita del sistema operativo Unix; il periodo più creativo fu il 1972.
- Il C derivò dal linguaggio **B** di Ken Thompson, a sua volta influenzato da **BCPL**.
- Fu progettato come linguaggio per implementare sistemi: doveva produrre programmi efficienti e vicini alla macchina, ma essere più espressivo e portabile dell'assembly.
- La riscrittura di parti importanti di Unix in C dimostrò che un sistema operativo poteva essere trasferito più facilmente tra macchine diverse.
- Nel 1978 Brian Kernighan e Dennis Ritchie pubblicarono *The C Programming Language*, il celebre libro “K&R”.
- Il linguaggio fu standardizzato da ANSI nel 1989 e poi da ISO; gli standard successivi hanno continuato a evolverlo.

## Perché il C è ancora usato

Il C rimane importante quando servono efficienza, controllo delle risorse, interoperabilità e portabilità su hardware molto diverso. Oggi viene usato soprattutto per:

- sistemi operativi e componenti di sistema: il kernel Linux è scritto principalmente in C;
- firmware, microcontrollori e sistemi embedded;
- sistemi operativi real-time, come Zephyr e FreeRTOS;
- driver e interfacce con l'hardware;
- librerie, runtime e interpreti che devono offrire un'interfaccia stabile e veloce;
- software nel quale memoria, tempi di esecuzione e dimensione del programma devono essere controllati con precisione.

Il C non è sempre la scelta più comoda per applicazioni web o programmi ad alto livello, perché richiede una gestione più attenta della memoria e offre meno protezioni automatiche rispetto a linguaggi più recenti.

## Errori concettuali comuni

- pensare che “formale” significhi soltanto “serio”: significa che il linguaggio è governato da regole precise;
- confondere sintassi corretta con programma logicamente corretto;
- pensare che “alto livello” significhi automaticamente “migliore” o “più potente”;
- considerare C un linguaggio di basso livello soltanto perché permette di accedere alla memoria;
- credere che compilato e interpretato siano due categorie assolute e senza soluzioni intermedie;
- attribuire l'invenzione del C a Brian Kernighan: Kernighan contribuì alla diffusione e al celebre libro, mentre il progettista principale del linguaggio fu Dennis Ritchie.

## Fonti

- [Dennis Ritchie, *The Development of the C Language* — Bell Labs](https://www.nokia.com/bell-labs/about/dennis-m-ritchie/chist.html)
- [Linguaggio usato dal kernel Linux — documentazione ufficiale](https://docs.kernel.org/process/programming-language.html)
- [Supporto del C in Zephyr — documentazione ufficiale](https://docs.zephyrproject.org/latest/develop/languages/c/index.html)
- [Modello di esecuzione di Python — documentazione ufficiale](https://docs.python.org/3/reference/executionmodel.html)
- [Estendere Python con C o C++ — documentazione ufficiale](https://docs.python.org/3/extending/extending.html)

## Collegamenti

- [[01 Struttura di un programma C|Struttura di un programma C]]
- [[02 Variabili costanti e tipi|Variabili, costanti e tipi]]
