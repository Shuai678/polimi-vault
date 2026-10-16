---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 1, PDF pp. 3-7, pagine stampate 13-17"
  - "Lezione 3, PDF pp. 3-5, pagine stampate 23-25"
---

# Funzioni

Stato: **da studiare**.

## Intuizione

Una funzione assegna a ciascun elemento di partenza un unico elemento di arrivo. Elementi di partenza diversi possono avere la stessa immagine.

## Definizione 1.1

Una funzione da $A$ a $B$ è una [[02 Relazioni Binarie|relazione]] $F\subseteq A\times B$ tale che

$$
\forall a\in A,\quad \exists! b\in B:\ (a,b)\in F.
$$

Il simbolo $\exists!$ significa «esiste uno e un solo».

- $A$ è il **dominio**.
- $B$ è il **codominio**.
- $F$ specifica gli abbinamenti.

Si scrive

$$
F:A\longrightarrow B,\qquad F(a)=b
$$

per indicare che $(a,b)\in F$.

L'esistenza impone un'immagine per ogni $a\in A$. L'unicità vieta due immagini diverse per lo stesso $a$. Non richiede che ogni elemento di $B$ venga raggiunto.

## Esempi del professore

### Colore della maglia

Assegnando a ogni persona il colore della propria maglia si ottiene una funzione, nell'ipotesi di un unico colore assegnato. Due persone con la stessa maglia possono avere la stessa immagine.

La relazione «avere la maglia dello stesso colore» tra persone non è in generale una funzione: una persona può essere collegata a più persone.

### Iniziale di un frutto

Nella Lezione 1:

$$
\begin{aligned}
A&=\{\text{ananas},\text{banana},\text{limone},\text{lampone}\},\\
B&=\{a,b,l\}.
\end{aligned}
$$

La funzione associa a ciascun frutto la propria iniziale:

$$
F=\{(\text{ananas},a),(\text{banana},b),
(\text{limone},l),(\text{lampone},l)\}.
$$

L'immagine $l$ è ripetuta, ma ogni frutto ha una sola immagine: si tratta comunque di una funzione.

## Il grafico come insieme di coppie

La Lezione 3 indica con $\Gamma(f)$ il grafico:

$$
\Gamma(f)=\{(a,f(a))\mid a\in A\}\subseteq A\times B.
$$

Per $f:\mathbb R\to\mathbb R$, $f(x)=x^2$:

$$
\Gamma(f)=\{(x,y)\in\mathbb R^2\mid y=x^2\}.
$$

Fissando $x$, esiste un solo valore $y=x^2$. Il grafico geometrico rappresenta le coppie del grafico insiemistico.

## Contare le coppie non basta

Se $A$ è finito e $F:A\to B$ è una funzione, il grafico ha esattamente una coppia per ciascun elemento di $A$:

$$
\#F=\#A.
$$

Questa è una condizione necessaria, ma da sola non è sufficiente.

Controesempio del tutor:

$$
A=\{1,2\},\quad B=\{a,b\},\quad
R=\{(1,a),(1,b)\}.
$$

Qui $\#R=\#A=2$, ma $1$ ha due immagini e $2$ non ne ha nessuna. Quindi $R$ non è una funzione da $A$ a $B$.

Se $\#F\ne\#A$, per insiemi finiti, si può concludere che $F$ non è una funzione. Il ragionamento usa la [[06 Implicazione e Contrapposizione|contrapposizione]].

## Procedimento per riconoscere una funzione

Per ciascun elemento del dominio:

1. si cercano le coppie che lo hanno come primo elemento;
2. si controlla che almeno una coppia esista;
3. si controlla che la seconda componente sia unica.

Per dimostrare che una relazione non è una funzione basta un elemento senza immagine oppure con due immagini distinte.

## Da dire all'orale

> Una funzione da un insieme A a un insieme B è una relazione che associa a ogni elemento di A uno e un solo elemento di B. Il dominio, il codominio e la regola di associazione fanno parte della specificazione della funzione.

## Collegamenti e fonti

- [[07 Iniettività]], [[08 Suriettività]], [[09 Biiettività]].
- [[11 Matrici come Funzioni e Indici]]: anche una matrice è definita come funzione.
- [[GAL 2026-2027 - 20260917 - LEZIONE 1.pdf#page=3|Lezione 1, pp. 3-7, stampate 13-17]].
- [[GAL 2026-2027 - 20260930 - LEZIONE 3.pdf#page=3|Lezione 3, pp. 3-5, stampate 23-25]], per il grafico e la sua funzione indicatrice.
