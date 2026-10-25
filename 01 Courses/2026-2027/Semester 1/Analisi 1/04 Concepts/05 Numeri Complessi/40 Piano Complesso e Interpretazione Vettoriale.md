---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF pp. 8-9
  - Libro, cap. 1.8.1, p. 20
---

# Piano complesso e interpretazione vettoriale

## Intuizione

Un numero reale richiede una sola coordinata e si rappresenta su una retta. Un numero complesso

$$
z=x+iy
$$

contiene invece due componenti reali: la parte reale $x$ e la parte immaginaria $y$. Per rappresentarlo geometricamente servono quindi due assi.

## Definizione formale

A ogni numero complesso $z=x+iy$ si associa il punto

$$
P_z=(x,y)\in\mathbb R^2,
$$

dove

$$
x=\operatorname{Re}z,
\qquad
y=\operatorname{Im}z.
$$

Il piano così interpretato è detto **piano complesso** o **piano di Argand-Gauss**.

### Da dire all'orale

> Il numero complesso $z=x+iy$ viene identificato con il punto $(x,y)$ del piano complesso: la parte reale è l'ascissa e la parte immaginaria è l'ordinata. Lo stesso numero può essere rappresentato dal vettore applicato nell'origine e avente estremo nel punto $(x,y)$.

## Rappresentazione nel piano

![[Assets/40 Piano Complesso - Punto e Vettore.svg|678]]

Nel grafico:

- l'asse orizzontale è l'**asse reale**;
- l'asse verticale è l'**asse immaginario**;
- il punto $P_z=(x,y)$ rappresenta il numero $z=x+iy$;
- il vettore dall'origine $O$ a $P_z$ rappresenta lo stesso numero complesso.

### Numeri reali e immaginari puri

Ogni numero reale $a$ si scrive come

$$
a=a+0i
$$

e corrisponde al punto $(a,0)$ dell'asse reale.

Ogni numero immaginario puro $ib$ si scrive come

$$
ib=0+ib
$$

e corrisponde al punto $(0,b)$ dell'asse immaginario.

## Interpretazione geometrica della somma

Siano

$$
z=x+iy,
\qquad
w=a+ib.
$$

La loro somma è

$$
z+w=(x+a)+i(y+b).
$$

Nel piano complesso questo equivale alla somma tra coppie ordinate:

$$
(x,y)+(a,b)=(x+a,y+b).
$$

![[Assets/40 Piano Complesso - Somma e Parallelogramma.svg|700]]

La diagonale verde rappresenta $z+w$. Lo stesso risultato si ottiene traslando il vettore di $w$ in modo che la sua origine coincida con l'estremo di $z$, oppure traslando $z$ all'estremo di $w$.

### Da dire all'orale

> Nel piano complesso la somma di due numeri corrisponde alla somma dei vettori associati e può essere costruita mediante la regola del parallelogramma.

## Condizioni

- Le coordinate $x,y,a,b$ devono essere reali.
- La coppia ordinata $(x,y)$ appartiene a $\mathbb R^2$, non a $\mathbb R$.
- Per rappresentare la somma non sono richieste condizioni di non nullità.

## Metodo

Per rappresentare $z=x+iy$:

1. si identifica $x=\operatorname{Re}z$;
2. si identifica $y=\operatorname{Im}z$;
3. si colloca il punto $(x,y)$ nel piano;
4. si traccia, se richiesto, il vettore dall'origine al punto.

Per rappresentare $z+w$:

1. si disegnano i vettori associati a $z$ e $w$;
2. si costruisce il parallelogramma avente tali vettori come lati;
3. la diagonale uscente dall'origine rappresenta $z+w$.

## Esempi

Il numero

$$
z=-3+2i
$$

corrisponde al punto

$$
P_z=(-3,2).
$$

La coordinata $-3$ impone uno spostamento di tre unità verso sinistra; la coordinata $2$ impone uno spostamento di due unità verso l'alto.

## Errori comuni

- Scambiare la parte reale con la parte immaginaria.
- Collocare un numero immaginario puro sull'asse reale.
- Scrivere $(x,y)\in\mathbb R$ invece di $(x,y)\in\mathbb R^2$.
- Confondere la parte immaginaria $y$ con il termine immaginario $iy$.
- Usare la regola del parallelogramma per il prodotto: essa rappresenta la somma.

## Connessioni

- L'identificazione utilizza la [[37 Unità Immaginaria e Forma Algebrica|forma algebrica]].
- La somma vettoriale rappresenta geometricamente le [[38 Operazioni con i Numeri Complessi|operazioni di somma]].
- La lunghezza del vettore è il [[41 Coniugato e Modulo dei Numeri Complessi|modulo del numero complesso]].
- L'angolo formato dal vettore con il semiasse reale positivo condurrà all'argomento.

## Prospettiva d'esame

Potenziale rilevanza d'esame: saper passare dalla forma algebrica alle coordinate, riconoscere gli assi reale e immaginario e interpretare geometricamente la somma senza confonderla con il prodotto.
