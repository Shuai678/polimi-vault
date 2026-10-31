---
course: Analisi 1
type: formula-sheet
updated: 2026-10-30
cssclasses:
  - formulario
---

# Goniometria per i numeri complessi

[[00 Indice Formulario|Indice del formulario]] · [[03 Numeri Complessi|Formulario dei numeri complessi]]

Formule e valori utili per passare dalla forma algebrica alla forma trigonometrica, trovare l'argomento e calcolare potenze e radici.

**In questa scheda:** [[#Angoli notevoli|Angoli notevoli]] · [[#Periodicità e angoli associati|Periodicità e simmetrie]] · [[#Come trovare l'argomento|Argomento e quadranti]] · [[#Identità goniometriche utili|Identità]] · [[#Applicazioni ai numeri complessi|Potenze e radici]]

Gli angoli nelle formule sono in **radianti**. I gradi nella tabella servono solo come riferimento:

$$
180^\circ=\pi\text{ radianti},
\qquad
\theta_{\mathrm{rad}}=\theta_{\mathrm{gradi}}\frac{\pi}{180}.
$$

## Dalla circonferenza al numero complesso

Sulla circonferenza unitaria il punto associato all'angolo $\theta$ ha coordinate **$(\cos\theta,\sin\theta)$**: prima il coseno, poi il seno.

Per $z=x+iy\neq0$, ponendo $r=\lvert z\rvert=\sqrt{x^2+y^2}>0$:

$$
\boxed{z=r(\cos\theta+i\sin\theta)=re^{i\theta}}
$$

$$
x=r\cos\theta,
\qquad y=r\sin\theta,
\qquad
\cos\theta=\frac{x}{r},
\qquad\sin\theta=\frac{y}{r}.
$$

Il numero $0$ ha modulo $0$ e **non ha argomento**. Approfondimento: [[48 Forma Trigonometrica dei Numeri Complessi]].

## Angoli notevoli

| Gradi | Radianti $\theta$ | $\cos\theta$ | $\sin\theta$ | $\tan\theta$ |
| :---: | :---: | :---: | :---: | :---: |
| $0^\circ$ | $0$ | $1$ | $0$ | $0$ |
| $30^\circ$ | $\pi/6$ | $\sqrt3/2$ | $1/2$ | $\sqrt3/3$ |
| $45^\circ$ | $\pi/4$ | $\sqrt2/2$ | $\sqrt2/2$ | $1$ |
| $60^\circ$ | $\pi/3$ | $1/2$ | $\sqrt3/2$ | $\sqrt3$ |
| $90^\circ$ | $\pi/2$ | $0$ | $1$ | Non definita |
| $120^\circ$ | $2\pi/3$ | $-1/2$ | $\sqrt3/2$ | $-\sqrt3$ |
| $135^\circ$ | $3\pi/4$ | $-\sqrt2/2$ | $\sqrt2/2$ | $-1$ |
| $150^\circ$ | $5\pi/6$ | $-\sqrt3/2$ | $1/2$ | $-\sqrt3/3$ |
| $180^\circ$ | $\pi$ | $-1$ | $0$ | $0$ |
| $210^\circ$ | $7\pi/6$ | $-\sqrt3/2$ | $-1/2$ | $\sqrt3/3$ |
| $225^\circ$ | $5\pi/4$ | $-\sqrt2/2$ | $-\sqrt2/2$ | $1$ |
| $240^\circ$ | $4\pi/3$ | $-1/2$ | $-\sqrt3/2$ | $\sqrt3$ |
| $270^\circ$ | $3\pi/2$ | $0$ | $-1$ | Non definita |
| $300^\circ$ | $5\pi/3$ | $1/2$ | $-\sqrt3/2$ | $-\sqrt3$ |
| $315^\circ$ | $7\pi/4$ | $\sqrt2/2$ | $-\sqrt2/2$ | $-1$ |
| $330^\circ$ | $11\pi/6$ | $\sqrt3/2$ | $-1/2$ | $-\sqrt3/3$ |
| $360^\circ$ | $2\pi$ | $1$ | $0$ | $0$ |

> [!tip] Memorizzare il primo quadrante
> Per $0,\pi/6,\pi/4,\pi/3,\pi/2$ i valori del seno sono $\sqrt0/2,\sqrt1/2,\sqrt2/2,\sqrt3/2,\sqrt4/2$. Quelli del coseno si leggono in ordine inverso. Negli altri quadranti cambiano i segni.

## Periodicità e angoli associati

Per ogni $k\in\mathbb Z$:

$$
\cos(\theta+2k\pi)=\cos\theta,
\qquad
\sin(\theta+2k\pi)=\sin\theta.
$$

$$
\tan(\theta+k\pi)=\tan\theta
\qquad\text{se }\cos\theta\neq0.
$$

**Seno e coseno hanno periodo $2\pi$; la tangente ha periodo $\pi$.** Per questo la sola tangente non distingue punti in quadranti opposti.

| Angolo | Coseno | Seno |
| --- | --- | --- |
| $-\alpha$ | $\cos\alpha$ | $-\sin\alpha$ |
| $\pi-\alpha$ | $-\cos\alpha$ | $\sin\alpha$ |
| $\pi+\alpha$ | $-\cos\alpha$ | $-\sin\alpha$ |
| $2\pi-\alpha$ | $\cos\alpha$ | $-\sin\alpha$ |
| $\pi/2-\alpha$ | $\sin\alpha$ | $\cos\alpha$ |
| $\pi/2+\alpha$ | $-\sin\alpha$ | $\cos\alpha$ |

**Esempio:** $5\pi/6=\pi-\pi/6$, quindi $\cos(5\pi/6)=-\sqrt3/2$ e $\sin(5\pi/6)=1/2$.

Per ridurre un angolo, aggiungere o sottrarre multipli di $2\pi$: per esempio $17\pi/4=4\pi+\pi/4$ ha lo stesso seno e coseno di $\pi/4$.

## Come trovare l'argomento

### Segni nei quadranti

| Quadrante | Angoli in $[0,2\pi)$ | $x$ e $\cos\theta$ | $y$ e $\sin\theta$ | $\tan\theta$ |
| :---: | :---: | :---: | :---: | :---: |
| I | $(0,\pi/2)$ | $+$ | $+$ | $+$ |
| II | $(\pi/2,\pi)$ | $-$ | $+$ | $-$ |
| III | $(\pi,3\pi/2)$ | $-$ | $-$ | $+$ |
| IV | $(3\pi/2,2\pi)$ | $+$ | $-$ | $-$ |

### Metodo pratico

Per $z=x+iy\neq0$:

1. Calcolare $r=\sqrt{x^2+y^2}$.
2. Cercare l'angolo con $\cos\theta=x/r$ e $\sin\theta=y/r$, usando tabella e segni.
3. Se serve l'**argomento principale**, scegliere il rappresentante in $(-\pi,\pi]$.

Qui indichiamo l'argomento principale con $\operatorname{Arg}z$. Tutti gli argomenti sono $\operatorname{Arg}z+2k\pi$, con $k\in\mathbb Z$.

Per passare da $[0,2\pi)$ a $(-\pi,\pi]$, basta sottrarre $2\pi$ agli angoli maggiori di $\pi$: per esempio $4\pi/3$ diventa $-2\pi/3$.

### Se l'angolo non è notevole: arcotangente

Poiché $\arctan t\in(-\pi/2,\pi/2)$, per $z\neq0$ si usa:

$$
\operatorname{Arg}(x+iy)=
\begin{cases}
\arctan(y/x), & x>0,\\[4pt]
\arctan(y/x)+\pi, & x<0,\ y\geq0,\\[4pt]
\arctan(y/x)-\pi, & x<0,\ y<0,\\[4pt]
\pi/2, & x=0,\ y>0,\\[4pt]
-\pi/2, & x=0,\ y<0.
\end{cases}
$$

Sugli assi: $\operatorname{Arg}(r)=0$, $\operatorname{Arg}(-r)=\pi$, $\operatorname{Arg}(ir)=\pi/2$, $\operatorname{Arg}(-ir)=-\pi/2$, per $r>0$.

> [!warning] Stesso rapporto, argomenti diversi
> $1+i$ e $-1-i$ hanno entrambi $y/x=1$, ma i loro argomenti principali sono rispettivamente $\pi/4$ e $-3\pi/4$. Controllare sempre il quadrante prima di usare $\arctan(y/x)$.

Approfondimenti: [[49 Determinazione dell'Argomento per Quadranti]] · [[69 Funzioni Goniometriche Inverse]].

## Identità goniometriche utili

### Identità fondamentale e tangente

$$
\boxed{\cos^2\theta+\sin^2\theta=1}
\qquad
\tan\theta=\frac{\sin\theta}{\cos\theta}
\quad(\cos\theta\neq0).
$$

### Addizione e sottrazione

$$
\begin{aligned}
\cos(\alpha+\beta)&=\cos\alpha\cos\beta-\sin\alpha\sin\beta,\\
\cos(\alpha-\beta)&=\cos\alpha\cos\beta+\sin\alpha\sin\beta,\\
\sin(\alpha+\beta)&=\sin\alpha\cos\beta+\cos\alpha\sin\beta,\\
\sin(\alpha-\beta)&=\sin\alpha\cos\beta-\cos\alpha\sin\beta.
\end{aligned}
$$

Sono le formule che permettono di riconoscere il prodotto di due numeri in forma trigonometrica: vedi [[D03 Formule di De Moivre per Prodotti e Potenze]].

### Duplicazione e bisezione

$$
\sin(2\theta)=2\sin\theta\cos\theta,
$$

$$
\cos(2\theta)=\cos^2\theta-\sin^2\theta
=2\cos^2\theta-1=1-2\sin^2\theta.
$$

$$
\cos^2\frac\theta2=\frac{1+\cos\theta}{2},
\qquad
\sin^2\frac\theta2=\frac{1-\cos\theta}{2}.
$$

Per ricavare seno e coseno dell'angolo dimezzato, prendere la radice e scegliere il **segno in base al quadrante di $\theta/2$**. Le formule sono utili quando nelle radici complesse compaiono angoli come $\pi/8$.

## Applicazioni ai numeri complessi

### Eulero, coniugato e rotazioni

$$
e^{i\theta}=\cos\theta+i\sin\theta,
\qquad
e^{-i\theta}=\cos\theta-i\sin\theta.
$$

Se $z=re^{i\theta}$, allora $\bar z=re^{-i\theta}$: il coniugato cambia il segno dell'angolo. Moltiplicare per $i=e^{i\pi/2}$ ruota di $\pi/2$ in senso antiorario; moltiplicare per $-1=e^{i\pi}$ ruota di $\pi$.

### Prodotto, quoziente e potenze

Per $z=re^{i\theta}$ e $w=Re^{i\varphi}$, con $r,R>0$:

$$
zw=rR\,e^{i(\theta+\varphi)},
\qquad
\frac zw=\frac rR\,e^{i(\theta-\varphi)}.
$$

Per $n\in\mathbb Z$ e $z\neq0$:

$$
\boxed{z^n=r^n\bigl(\cos(n\theta)+i\sin(n\theta)\bigr)}.
$$

Gli angoli risultanti si possono ridurre modulo $2\pi$. Vedi [[51 Formule di De Moivre - Prodotto e Quoziente]] e [[52 Formula di De Moivre per le Potenze Complesse]].

**Esempio: $(1+i)^6$.** Poiché $1+i=\sqrt2\,e^{i\pi/4}$:

$$
(1+i)^6=(\sqrt2)^6e^{i6\pi/4}
=8e^{i3\pi/2}=-8i.
$$

### Radici ennesime

Per $w=Re^{i\varphi}\neq0$ e $n\geq1$ intero, le soluzioni di $z^n=w$ sono:

$$
\boxed{
z_k=R^{1/n}\left[
\cos\left(\frac{\varphi+2k\pi}{n}\right)
+i\sin\left(\frac{\varphi+2k\pi}{n}\right)
\right],\quad k=0,\ldots,n-1.
}
$$

Gli angoli di radici consecutive differiscono di $2\pi/n$. Se $w=0$, l'unica soluzione è $z=0$. Vedi [[53 Radici Ennesime Complesse]].

> [!warning] Prima aggiungere, poi dividere
> Per trovare tutte le radici bisogna dividere per $n$ l'intero angolo $\varphi+2k\pi$. Dividere soltanto $\varphi$ produce una sola radice.

**Esempio: $z^3=-8$.** Scrivere $-8=8e^{i\pi}$: il modulo delle radici è $2$ e gli angoli sono $\pi/3$, $\pi$ e $5\pi/3$.

| $k$ | Angolo | Radice in forma algebrica |
| :---: | :---: | :---: |
| $0$ | $\pi/3$ | $1+i\sqrt3$ |
| $1$ | $\pi$ | $-2$ |
| $2$ | $5\pi/3$ | $1-i\sqrt3$ |

Per scrivere l'ultima radice con argomento principale si usa $-\pi/3$ al posto di $5\pi/3$: il numero complesso è lo stesso.

---

[[03 Numeri Complessi|← Numeri complessi]] · [[00 Indice Formulario#Indice rapido|↑ Indice]]
