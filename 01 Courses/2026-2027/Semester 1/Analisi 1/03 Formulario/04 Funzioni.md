---
course: Analisi 1
type: formula-sheet
updated: 2026-10-29
cssclasses:
  - formulario
---

# Funzioni

[[00 Indice Formulario|Indice del formulario]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map/00 Course Map|Corso]]

**In questa scheda:** [[#Definizione e dominio|Definizione e dominio]] · [[#Proprietà delle funzioni|Proprietà delle funzioni]] · [[#Composizione e inverse|Composizione e inverse]]

## Definizione e dominio

### Funzione, immagine e grafico

[[55 Funzioni Dominio Codominio e Immagine|Funzione e immagine]] · [[57 Grafico di una Funzione|grafico]]

$f:A\to B$ associa a ogni $x\in A$ **un solo** $f(x)\in B$.

$$
\operatorname{Im}f=\{f(x):x\in A\},\qquad
G(f)=\{(x,f(x)):x\in A\}.
$$

### Dominio naturale

[[60 Dominio Naturale di una Funzione|Dominio naturale]]

| Espressione | Vincolo |
| --- | --- |
| Denominatore | $\neq0$ |
| Radicando di indice pari | $\geq0$ |
| Argomento di un logaritmo | $>0$ |

> [!warning] Dopo le semplificazioni
> Conservare tutti i vincoli del dominio originale.

## Proprietà delle funzioni

### Iniettività, suriettività e biiettività

[[65 Funzioni Iniettive e Biiettive|Iniettività]] · [[56 Suriettività|suriettività]]

**Iniettiva**

$$
f(x_1)=f(x_2)\Rightarrow x_1=x_2.
$$

**Suriettiva**

$$
\forall y\in B\ \exists x\in A:\ f(x)=y.
$$

**Biiettiva:** iniettiva e suriettiva.

### Limitatezza ed estremi

[[59 Funzioni Limitate ed Estremi di Funzione|Limitatezza ed estremi]]

**Limitata**

$$
\exists K>0\ \forall x\in A:\ \lvert f(x)\rvert\leq K.
$$

$$
\sup_A f=\sup\operatorname{Im}f.
$$

Il supremo è un **massimo solo se il valore è assunto**.

### Parità e periodicità

[[61 Funzioni Pari e Dispari|Parità]] · [[63 Funzioni Periodiche|periodicità]]

**Parità** — Il dominio deve essere simmetrico.

$$
\begin{aligned}
f\text{ pari}&\iff f(-x)=f(x),\\
f\text{ dispari}&\iff f(-x)=-f(x).
\end{aligned}
$$

**Periodicità** — Con $T>0$, il dominio è invariato dalla traslazione e

$$
f(x+T)=f(x).
$$

### Monotonia

[[62 Funzioni Monotone|Monotonia]]

Per ogni $x_1<x_2$ nel dominio:

| Proprietà | Confronto |
| --- | --- |
| Crescente | $f(x_1)\leq f(x_2)$ |
| Strettamente crescente | $f(x_1)<f(x_2)$ |
| Decrescente | $f(x_1)\geq f(x_2)$ |
| Strettamente decrescente | $f(x_1)>f(x_2)$ |

## Composizione e inverse

### Composizione

[[64 Composizione di Funzioni|Composizione]]

$$
(g\circ f)(x)=g(f(x)).
$$

$$
D(g\circ f)=\{x\in D(f):f(x)\in D(g)\}.
$$

### Inversa e monotonia

[[66 Funzione Inversa|Inversa]] · [[67 Monotonia e Funzione Inversa|monotonia dell'inversa]]

**Ipotesi:** $f$ iniettiva.

$$
f^{-1}:\operatorname{Im}f\to A,\qquad f^{-1}(f(x))=x.
$$

**Stretta monotonia $\Rightarrow$ iniettività.** L'inversa conserva il verso della monotonia.

### Potenze e radici inverse

[[68 Funzioni Potenza e Radice come Inversa|Potenze e radici inverse]]

- **$m$ dispari:** $x^m$ è invertibile su $\mathbb R$.
- **$m$ pari:** restringere il dominio, per esempio a $[0,+\infty)$, per ottenere la radice principale.

### Inverse goniometriche

[[69 Funzioni Goniometriche Inverse|Inverse goniometriche]]

| Inversa | Dominio | Immagine |
| --- | --- | --- |
| $\arcsin$ | $[-1,1]$ | $[-\pi/2,\pi/2]$ |
| $\arccos$ | $[-1,1]$ | $[0,\pi]$ |
| $\arctan$ | $\mathbb R$ | $(-\pi/2,\pi/2)$ |

---

[[03 Numeri Complessi|← Numeri Complessi]] · [[00 Indice Formulario#Indice rapido|↑ Indice]] · [[05 Successioni e Limiti|Successioni e Limiti →]]
