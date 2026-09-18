---
course: Analisi 1
type: prelezione-temporanea
status: temporaneo
date: 2026-09-16
previsione: true
sources:
  - "Lezione 01 del professore"
  - "Programma svolto 2025-2026"
  - "Biagi-Punzo, capitolo 1"
---

# Prelezione temporanea - possibile Lezione 02

> [!warning] Contenuto non ancora confermato
> Non è disponibile il PDF della Lezione 02. Questa nota è una previsione costruita dall'ordine della Lezione 01, dal programma dell'anno precedente e dal libro di testo. Dopo la lezione reale dovrà essere verificata e sostituita da una nota definitiva.

## Panoramica prevista

- **Lezione:** possibile Lezione 02, durata prevista di tre ore.
- **Nucleo più probabile:** ordinamento dei numeri reali, maggioranti e minoranti, insiemi limitati, massimo e minimo, estremo superiore ed estremo inferiore, completezza di $\mathbb{R}$.
- **Possibile prosecuzione:** potenze e logaritmi, se il professore mantiene un ritmo rapido.
- **Meno probabile nella stessa lezione:** grandezze goniometriche e valore assoluto.
- **Posizione nel corso:** passaggio dai fondamenti logici e dai metodi di dimostrazione alle proprietà strutturali dei numeri reali.

## Perché questa previsione

La Lezione 01 arriva alla disuguaglianza di Bernoulli, corrispondente alla fine della prima parte del capitolo 1 del libro. Nel programma dell'anno precedente, gli argomenti immediatamente successivi sono:

1. proprietà di campo ordinato;
2. maggioranti e minoranti;
3. insiemi limitati;
4. massimo e minimo;
5. estremo superiore ed estremo inferiore;
6. proprietà di completezza di $\mathbb{R}$;
7. potenze e logaritmi.

## Prerequisiti da avere pronti

- [[06 Numeri Reali e Irrazionali|Numeri reali e irrazionali]];
- [[09 Sottoinsiemi e Inclusione|sottoinsiemi e inclusione]];
- [[11 Predicati e Variabili Libere|quantificatori e predicati]];
- [[15 Implicazione Logica|implicazione logica]];
- [[19 Controesempio|controesempio]].

La connessione principale è questa: per definire un maggiorante o un estremo superiore bisogna formulare una proprietà valida per **ogni** elemento di un insieme. Per negarla o costruire un controesempio servono quindi i quantificatori studiati nella Lezione 01.

## Priorità per la prelezione

### Priorità A — molto probabile

#### 1. Maggioranti e minoranti

Sia $A\subseteq\mathbb{R}$.

Un numero $M\in\mathbb{R}$ è un **maggiorante** di $A$ se

$$
\forall x\in A,\quad x\leq M.
$$

Un numero $m\in\mathbb{R}$ è un **minorante** di $A$ se

$$
\forall x\in A,\quad m\leq x.
$$

##### Esempio completo

Consideriamo

$$
A=\{1,2,3\}.
$$

Il numero $3$ è un maggiorante, perché ogni elemento di $A$ è minore o uguale a $3$:

$$
1\leq 3,\qquad 2\leq 3,\qquad 3\leq 3.
$$

Anche $4$, $5$ e ogni numero reale maggiore di $3$ sono maggioranti. Il numero $2$ non è un maggiorante, perché $3\in A$ ma $3\nleq 2$.

Analogamente, $1$ è un minorante e lo sono anche $0$, $-1$ e tutti i numeri reali minori di $1$.

#### 2. Insiemi limitati

Un insieme $A\subseteq\mathbb{R}$ è **limitato superiormente** se possiede almeno un maggiorante. È **limitato inferiormente** se possiede almeno un minorante. È **limitato** se è limitato sia superiormente sia inferiormente.

##### Esempio completo

L'insieme $A=\{1,2,3\}$ è limitato superiormente da $3$ e limitato inferiormente da $1$; quindi è limitato.

L'insieme $B=\mathbb{N}$ è limitato inferiormente, per esempio da $0$, ma non è limitato superiormente: scelto un qualunque candidato $M\in\mathbb{R}$, esiste un numero naturale maggiore di $M$.

#### 3. Massimo e minimo

Il numero $x_M$ è il **massimo** di $A$ se:

1. $x_M\in A$;
2. $x\leq x_M$ per ogni $x\in A$.

Il numero $x_m$ è il **minimo** di $A$ se:

1. $x_m\in A$;
2. $x_m\leq x$ per ogni $x\in A$.

##### Esempio completo

Per $A=\{1,2,3\}$ si ha

$$
\max A=3,\qquad \min A=1.
$$

Il numero $4$ è un maggiorante di $A$, ma non è il massimo perché $4\notin A$.

#### 4. Estremo superiore ed estremo inferiore

L'**estremo superiore** di $A$, indicato con $\sup A$, è il più piccolo tra tutti i maggioranti di $A$.

L'**estremo inferiore** di $A$, indicato con $\inf A$, è il più grande tra tutti i minoranti di $A$.

##### Esempio completo: estremo senza massimo

Consideriamo

$$
A=\{x\in\mathbb{R}:0<x<1\}.
$$

Il numero $1$ è un maggiorante perché ogni $x\in A$ soddisfa $x<1$, quindi anche $x\leq 1$.

Nessun numero minore di $1$ è un maggiorante. Infatti, se $0<M<1$, il numero

$$
x=\frac{M+1}{2}
$$

soddisfa

$$
M<x<1.
$$

Quando $M\leq 0$, basta invece scegliere, per esempio, $x=\frac12$. In entrambi i casi esiste un elemento di $A$ maggiore di $M$; dunque $M$ non è un maggiorante.

Pertanto

$$
\sup A=1.
$$

Tuttavia $1\notin A$, quindi $A$ non possiede massimo. Analogamente,

$$
\inf A=0,
$$

ma $A$ non possiede minimo perché $0\notin A$.

> [!important] Distinzione essenziale
> Il massimo, se esiste, deve appartenere all'insieme. L'estremo superiore può non appartenere all'insieme.

#### 5. Completezza dei numeri reali

La proprietà di completezza afferma che ogni sottoinsieme non vuoto di $\mathbb{R}$ limitato superiormente possiede estremo superiore in $\mathbb{R}$.

##### Esempio che mostra il ruolo di $\mathbb{R}$

Consideriamo l'insieme

$$
A=\{q\in\mathbb{Q}:q^2<2\}.
$$

L'insieme è non vuoto, perché $0\in A$, ed è limitato superiormente, per esempio da $2$. Il confine superiore naturale è $\sqrt{2}$.

In $\mathbb{R}$ esiste quindi

$$
\sup A=\sqrt{2}.
$$

Ma $\sqrt{2}\notin\mathbb{Q}$. Questo esempio mostra che i numeri razionali hanno dei “buchi”, mentre i numeri reali sono completi.

### Priorità B — possibile prosecuzione

#### 6. Potenze

Il professore potrebbe riprendere le potenze con esponente naturale, intero e razionale, chiarendo quali condizioni servono sulla base.

Esempio: per $a>0$ e $n\in\mathbb{N}\setminus\{0\}$,

$$
a^{1/n}=\sqrt[n]{a}.
$$

La condizione $a>0$ permette di definire senza ambiguità le potenze con esponente reale nel percorso standard del corso.

#### 7. Logaritmi

Il logaritmo risponde alla domanda: “a quale esponente devo elevare la base per ottenere un certo numero?”. Per $a>0$, $a\neq 1$ e $x>0$,

$$
y=\log_a x \quad\Longleftrightarrow\quad a^y=x.
$$

Le condizioni sulla base e sull'argomento sono essenziali.

### Priorità C — solo se il ritmo è molto rapido

- grandezze goniometriche;
- valore assoluto.

Questi argomenti non fanno parte del nucleo principale di questa prelezione, perché senza il PDF della Lezione 02 non è prudente anticipare troppo.

## Relazione tra gli argomenti

La catena concettuale prevista è:

**ordine in $\mathbb{R}$ → maggioranti e minoranti → insiemi limitati → massimo e minimo → estremo superiore e inferiore → completezza di $\mathbb{R}$.**

Ogni passaggio risponde a una domanda nuova:

1. come si confrontano i numeri reali?
2. esistono numeri che stanno sopra o sotto tutto un insieme?
3. l'insieme ha un elemento più grande o più piccolo?
4. se tali elementi non esistono, esiste almeno un confine ottimale?
5. perché questo confine esiste nei numeri reali?

## Difficoltà previste

- confondere un maggiorante con il massimo;
- credere che $\sup A$ debba appartenere ad $A$;
- dimenticare le condizioni “insieme non vuoto” e “limitato superiormente” nella proprietà di completezza;
- usare esempi numerici senza dimostrare una proprietà valida per ogni elemento;
- confondere $\sup A$ con il più grande elemento dell'insieme.

## Approfondimento dal libro

- Capitolo 1, §1.3, pp. 9-11: estremo superiore, estremo inferiore e completezza.
- Capitolo 1, §1.4, pp. 11-12: potenze.
- Capitolo 1, §1.5, pp. 12-13: logaritmi.

## Piano interattivo della prelezione

1. maggioranti, minoranti e insiemi limitati;
2. massimo e minimo;
3. estremo superiore ed estremo inferiore;
4. completezza di $\mathbb{R}$;
5. soltanto se necessario: potenze e logaritmi.

Ogni modulo verrà studiato separatamente e verificato con domande concettuali prima di passare al successivo.

## Dopo la lezione reale

- confrontare questa previsione con il PDF o con gli appunti effettivi;
- mantenere soltanto gli argomenti realmente svolti;
- creare o aggiornare i Concept definitivi solo dopo la verifica della comprensione;
- non usare questa nota temporanea come prova di ciò che il professore ha effettivamente spiegato.
