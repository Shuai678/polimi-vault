---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 05, PDF p. 9
  - Libro, §2.3.5, pp. 51-52
---

# Funzioni periodiche

## Definizione

Sia $f:A\to\mathbb R$. Un numero $T>0$ è un **periodo** di $f$ se il dominio è compatibile con la traslazione di $T$ e

$$
f(x+T)=f(x)
$$

per ogni $x$ per cui i due membri sono definiti. Nei domini usuali delle funzioni periodiche, come $A=\mathbb R$, ciò vale per ogni $x\in A$.

La funzione si dice **periodica** se possiede almeno un periodo positivo.

![[63 Funzioni Periodiche.svg|674]]

## Interpretazione geometrica

Il tratto di grafico contenuto in un intervallo lungo $T$ si ripete identico dopo una traslazione orizzontale di $T$. Per calcolare la funzione in $x+T$ basta quindi conoscere il valore in $x$.

### Da dire all'orale

> Una funzione è periodica se esiste $T>0$ tale che, traslando l'argomento di $T$, il valore non cambia: $f(x+T)=f(x)$ per ogni punto ammesso dal dominio.

## Esempi fondamentali

Per seno e coseno,

$$
\sin(x+2\pi)=\sin x,
\qquad
\cos(x+2\pi)=\cos x.
$$

Quindi $2\pi$, $4\pi$, $6\pi$, e in generale $2k\pi$ con $k\in\mathbb N$ positivo, sono periodi.

Per la tangente,

$$
\tan(x+\pi)=\tan x,
$$

quindi $\pi$, $2\pi$, $3\pi$, e in generale $k\pi$, sono periodi.

## Periodo fondamentale

> [!info] Precisazione dal libro
> Se tra tutti i periodi positivi esiste il più piccolo, esso viene chiamato **periodo fondamentale**. Per $\sin x$ e $\cos x$ è $2\pi$; per $\tan x$ è $\pi$.

Se $T$ è un periodo, ogni multiplo intero positivo $nT$ è ancora un periodo. Il periodo fondamentale non esiste per ogni funzione periodica: per esempio, una funzione costante ha come periodo ogni $T>0$, quindi non ha un minimo positivo.

## Come verificare una periodicità

1. Proporre un candidato $T>0$.
2. Controllare che la traslazione rispetti il dominio.
3. Calcolare e semplificare $f(x+T)$.
4. Mostrare che il risultato coincide con $f(x)$ per ogni $x$ ammesso.
5. Se si cerca il periodo fondamentale, dimostrare anche che nessun periodo positivo più piccolo funziona.

## Errori comuni

- Verificare l'uguaglianza soltanto in un punto.
- Dimenticare la condizione $T>0$.
- Chiamare fondamentale un periodo senza provare che è il più piccolo positivo.
- Confondere periodicità con simmetria pari o dispari.
- Trascurare i punti esclusi dal dominio, particolarmente per la tangente.

## Connessioni

- La ripetizione si riconosce nel [[57 Grafico di una Funzione|grafico]].
- Le funzioni trigonometriche forniscono gli esempi principali.
- La periodicità permette di ridurre lo studio a un solo intervallo di lunghezza $T$.

## Prospettiva d'esame

Per provare che un numero è un periodo occorre un'identità valida per ogni $x$ del dominio; osservare alcuni valori o un disegno non basta.
