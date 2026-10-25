---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF p. 13
---

# Equazioni in una variabile complessa

## Intuizione

Un'equazione complessa equivale a due equazioni reali: due numeri complessi sono uguali se e solo se coincidono sia le loro parti reali sia le loro parti immaginarie.

## Metodo

1. Porre $z=x+iy$, con $x,y\in\mathbb R$.
2. Sostituire $\operatorname{Re}z=x$ e $\overline z=x-iy$.
3. Sviluppare le operazioni usando $i^2=-1$.
4. Raccogliere separatamente parte reale e parte immaginaria.
5. Imporre che entrambe siano nulle.
6. Risolvere il sistema reale ottenuto.

### Da dire all'orale

> Scrivendo $z=x+iy$, un'equazione in una variabile complessa si trasforma in un sistema di due equazioni reali nelle variabili $x$ e $y$, ottenuto uguagliando separatamente parte reale e parte immaginaria.

## Esempio della lezione

Consideriamo

$$
z^2+2\operatorname{Re}z+\overline z=0.
$$

Ponendo $z=x+iy$,

$$
(x+iy)^2+2x+x-iy=0.
$$

Poiché

$$
(x+iy)^2=x^2+2xyi-y^2,
$$

si ottiene

$$
(x^2-y^2+3x)+i(2xy-y)=0.
$$

Quindi

$$
\begin{cases}
x^2-y^2+3x=0,\\
2xy-y=0.
\end{cases}
$$

La seconda equazione diventa

$$
y(2x-1)=0,
$$

perciò si distinguono due casi.

Se $y=0$, allora

$$
x^2+3x=x(x+3)=0,
$$

da cui $x=0$ oppure $x=-3$.

Se $x=\frac12$, allora

$$
\frac14-y^2+\frac32=0
\Longleftrightarrow
y^2=\frac74,
$$

da cui $y=\pm\frac{\sqrt7}{2}$.

Le soluzioni sono

$$
z_1=0,
\quad
z_2=-3,
\quad
z_3=\frac12+i\frac{\sqrt7}{2},
\quad
z_4=\frac12-i\frac{\sqrt7}{2}.
$$

## Condizioni

L'uguaglianza $A+iB=0$ equivale ad $A=0$ e $B=0$ quando $A,B\in\mathbb R$.

## Errori comuni

- Risolvere soltanto l'equazione della parte reale.
- Dimenticare il termine $2xyi$ nello sviluppo del quadrato.
- Dividere per $y$ nell'equazione $y(2x-1)=0$, perdendo il caso $y=0$.
- Ricostruire in modo scorretto $z=x+iy$ dalle soluzioni del sistema.

## Connessioni

- Usa [[37 Unità Immaginaria e Forma Algebrica|forma algebrica]], [[38 Operazioni con i Numeri Complessi|operazioni]] e [[44 Proprietà del Coniugato|coniugato]].
- Trasforma un problema complesso in un sistema reale.

## Prospettiva d'esame

Potenziale rilevanza d'esame: tradurre correttamente un'equazione complessa in un sistema reale senza perdere casi durante la fattorizzazione.
