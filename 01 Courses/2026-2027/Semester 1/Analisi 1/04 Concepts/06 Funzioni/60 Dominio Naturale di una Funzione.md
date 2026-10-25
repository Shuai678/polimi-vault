---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 05, PDF pp. 4-5
  - Libro, §2.3.1, p. 39
---

# Dominio naturale di una funzione

## Definizione

Quando una funzione reale viene assegnata soltanto mediante un'espressione analitica, senza dichiarare esplicitamente il dominio, si assume come **dominio naturale** o **campo di esistenza** il più grande sottoinsieme di $\mathbb R$ sul quale l'espressione ha significato reale.

Il codominio viene di norma sottinteso come $\mathbb R$.

### Da dire all'orale

> Il dominio naturale di un'espressione è il più grande insieme di numeri reali per i quali tutte le operazioni presenti risultano definite.

## Vincoli fondamentali

Nel determinare il dominio occorre imporre simultaneamente tutti i vincoli:

- un denominatore deve essere diverso da zero;
- il radicando di una radice di indice pari deve essere maggiore o uguale a zero;
- l'argomento di un logaritmo reale deve essere strettamente positivo;
- eventuali condizioni ulteriori devono essere intersecate tra loro.

## Esempi della lezione

### Radice quarta

Per

$$
f(x)=\sqrt[4]{1-x}
$$

occorre imporre

$$
1-x\geq0,
$$

quindi

$$
D(f)=(-\infty,1].
$$

### Logaritmo

Per

$$
g(x)=\log(x-7)
$$

occorre

$$
x-7>0,
$$

da cui

$$
D(g)=(7,+\infty).
$$

### Esponenziale

Per

$$
h(x)=2^x
$$

non compaiono restrizioni sulla variabile reale, dunque

$$
D(h)=\mathbb R.
$$

## Dominio dichiarato e dominio naturale

Il dominio naturale riguarda la formula isolata. Una funzione può però essere dichiarata su un sottoinsieme più piccolo.

Per esempio, la stessa espressione $x^2$ può definire funzioni diverse:

$$
f:\mathbb R\to\mathbb R,
\qquad f(x)=x^2,
$$

oppure

$$
g:[0,+\infty)\to\mathbb R,
\qquad g(x)=x^2.
$$

Formula e funzione non sono sinonimi: dominio e codominio fanno parte della definizione della funzione.

## Procedura operativa

1. Elencare tutte le operazioni che possono introdurre vincoli.
2. Scrivere una condizione per ciascuna di esse.
3. Risolvere le condizioni.
4. Intersecare gli insiemi ottenuti.
5. Esprimere il risultato con intervalli o notazione insiemistica.
6. Conservare il dominio anche dopo eventuali semplificazioni algebriche.

## Errori comuni

- Scrivere automaticamente $D(f)=\mathbb R$ perché non è stato dichiarato un dominio.
- Usare $\geq0$ per l'argomento del logaritmo, che deve invece essere $>0$.
- Richiedere radicando positivo anche per una radice dispari.
- Unire i vincoli quando devono valere tutti insieme: normalmente si prende l'intersezione.
- Perdere punti esclusi dopo una semplificazione formale.

## Connessioni

- Precisa il ruolo del dominio in [[55 Funzioni Dominio Codominio e Immagine|una funzione]].
- Usa le condizioni di esistenza di [[33 Radice Ennesima Reale|radici]], [[36 Logaritmi|logaritmi]] e frazioni.
- Sarà indispensabile nella [[64 Composizione di Funzioni|composizione di funzioni]].

## Prospettiva d'esame

Il dominio è il primo controllo di ogni esercizio su funzioni: deve essere determinato prima di equazioni, composizioni, inverse o studio del grafico.
