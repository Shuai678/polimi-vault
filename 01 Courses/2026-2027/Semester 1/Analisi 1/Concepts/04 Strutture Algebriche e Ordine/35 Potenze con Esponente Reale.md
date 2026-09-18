---
course: Analisi 1
type: concept
status: da-verificare
source:
  - Lezione 02, PDF pp. 27-30
  - Libro, cap. 1.4
---

# Potenze con esponente reale

## Intuizione

Un esponente reale può essere approssimato arbitrariamente mediante esponenti razionali. Le corrispondenti potenze razionali determinano un unico valore reale grazie alla completezza di $\mathbb{R}$.

## Definizione formale

Siano $a>1$ e $b\in\mathbb{R}$. Consideriamo

$$
S_b=\{a^r:r\in\mathbb{Q},\ r<b\}.
$$

Si definisce

$$
a^b=\sup S_b.
$$

Per $a=1$ si pone

$$
1^b=1.
$$

Per $0<a<1$, ponendo $c=1/a>1$, si definisce

$$
a^b=\frac1{c^b}.
$$

Equivalentemente, il valore può essere descritto mediante l'estremo inferiore delle opportune potenze razionali.

### Da dire all'orale

> Per una base positiva e un esponente reale, la potenza viene definita mediante le potenze con esponente razionale che approssimano l'esponente reale; per $a>1$, $a^b$ è l'estremo superiore delle potenze $a^r$ con $r\in\mathbb{Q}$ e $r<b$.

## Notazione

- $a>0$ è la base.
- $b\in\mathbb{R}$ è l'esponente reale.
- $r\in\mathbb{Q}$ è un'approssimazione razionale dell'esponente.
- $S_b$ raccoglie le potenze razionali con esponente inferiore a $b$.

## Condizioni

- La definizione uniforme per ogni esponente reale richiede $a>0$.
- Per $a>1$, l'insieme $S_b$ deve essere non vuoto e limitato superiormente.
- Le basi negative consentono soltanto alcuni esponenti reali e non ammettono una definizione reale uniforme.

## Metodo / Dimostrazione

### Esistenza per $a>1$

Per la densità di $\mathbb{Q}$ in $\mathbb{R}$ esiste un razionale $r<b$, quindi $S_b\neq\varnothing$.

Sempre per densità, scegliamo $q\in\mathbb{Q}$ con $q>b$. Poiché $a>1$, la potenza razionale è crescente rispetto all'esponente. Per ogni $r<b<q$ si ha

$$
a^r<a^q.
$$

Quindi $a^q$ è un maggiorante di $S_b$. L'insieme è non vuoto e limitato superiormente; per la completezza di $\mathbb{R}$ esiste $\sup S_b$, che viene definito come $a^b$.

### Approssimazioni decimali

Sia $b_k$ la successione delle troncature decimali proprie di $b$. Ogni $b_k$ è razionale e le potenze $a^{b_k}$ approssimano il valore $a^b$.

Per esempio, se

$$
b=1{,}414213\ldots,
$$

si usano gli esponenti $1$, $1{,}4$, $1{,}41$, $1{,}414$, e così via.

## Proprietà

Per $a,c>0$ e $b,d\in\mathbb{R}$:

$$
a^b a^d=a^{b+d},
$$

$$
\frac{a^b}{a^d}=a^{b-d},
$$

$$
(a^b)^d=a^{bd},
$$

$$
(ac)^b=a^b c^b.
$$

Inoltre $a^b>0$ per ogni $b\in\mathbb{R}$.

## Monotonia rispetto all'esponente

- Se $a>1$, da $b<d$ segue $a^b<a^d$.
- Se $0<a<1$, da $b<d$ segue $a^b>a^d$.
- Se $a=1$, la potenza vale sempre $1$.

## Errori comuni

- Interpretare un esponente irrazionale come un numero finito di moltiplicazioni.
- Confondere una troncatura razionale con l'esponente reale.
- Dimenticare la condizione $a>0$.
- Usare la completezza senza verificare non vacuità e limitatezza dell'insieme ausiliario.
- Confondere i ruoli della densità e della completezza.

## Connessioni

- [[32 Densità dei Razionali nei Reali|La densità]] fornisce esponenti razionali arbitrariamente vicini a $b$.
- [[34 Potenze con Esponente Razionale|Le potenze razionali]] definiscono le approssimazioni.
- [[27 Completezza dei Numeri Reali|La completezza]] garantisce l'esistenza dell'estremo che definisce il valore.
- [[26 Estremo Superiore e Inferiore|L'estremo superiore]] costruisce il valore finale per $a>1$.

## Prospettiva d'esame

Occorre saper spiegare separatamente il ruolo della densità, che produce approssimazioni razionali, e quello della completezza, che garantisce l'esistenza del valore reale limite.

## Sintassi LaTeX Suite

Le formule sono scritte con sintassi già espansa e renderizzabile, tra cui $a^b$, $\mathbb{Q}$, $\mathbb{R}$ e $\sup S_b$.
