---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D9
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 9"
  - "76 Teorema del Limite delle Successioni Monotone"
  - "Appunti del docente, teorema delle successioni monotome.pdf, pp. 1-3"
  - "AM1 L7 26-27.pdf.pdf, pp. 1-3"
cssclasses:
  - formulario
---

# D9 — Regolarità delle Successioni Monotone

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D9** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Ogni successione reale monotona è regolare, cioè ammette limite finito o infinito.

$$
\lim_{n\to+\infty}a_n=\ell\in\overline{\mathbb R}.
$$

Nella dimostrazione gli indici sono $n\in\mathbb N$ e partono da $0$: il primo termine è $a_0$.

- Se è crescente, il limite è $\sup_{n\in\mathbb N}a_n$: finito se è limitata superiormente, $+\infty$ altrimenti.
- Se è decrescente, il limite è $\inf_{n\in\mathbb N}a_n$: finito se è limitata inferiormente, $-\infty$ altrimenti.

Una successione monotona e limitata converge quindi a un numero reale.

## Idea della dimostrazione

Nel caso crescente e limitato, la proprietà del supremo trova un termine vicino al limite; la monotonia mantiene vicini anche tutti quelli successivi. Nel caso crescente e illimitato, la non limitatezza trova un termine sopra una soglia arbitraria; la monotonia mantiene sopra la soglia tutti i termini successivi. Per le successioni decrescenti il ragionamento è analogo.

## Dimostrazione

Si distinguono due casi: successione **limitata** e successione **illimitata**. Per ciascun caso si sviluppa prima la dimostrazione per una successione crescente; il caso decrescente è analogo.

### 1. Successione limitata

Si consideri inizialmente una successione **crescente e limitata**. Per monotonia è automaticamente limitata dal basso:

$$
a_n\geq a_0\qquad\forall n\in\mathbb N.
$$

> [!note] Limitatezza inferiore
> Essere crescente significa $a_0\leq a_1\leq a_2\leq\cdots$: nessun termine scende sotto il primo. Quindi $a_0$ è un minorante dell’insieme dei valori della successione. Per avere la limitatezza basta richiedere anche quella dall’alto.

Si pone

$$
\ell=\sup_{n\in\mathbb N}a_n\in\mathbb R\cup\{+\infty\}.
$$

Nel caso in esame, per ipotesi $a_n$ è limitata dall’alto: l’insieme $\{a_n:n\in\mathbb N\}$ è quindi non vuoto e limitato superiormente. Per l’**assioma dell’estremo superiore**, cioè la completezza di $\mathbb R$, il suo supremo esiste ed è finito:

$$
\ell=\sup_{n\in\mathbb N}a_n\in\mathbb R.
$$

Per definizione di estremo superiore, **$\ell$ è un maggiorante** dell’insieme dei valori della successione:

$$
a_n\leq\ell\qquad\forall n\in\mathbb N.
\tag{1}
$$

Inoltre, per ogni $\varepsilon>0$, il numero $\ell-\varepsilon$ **non è un maggiorante**: altrimenti esisterebbe un maggiorante più piccolo di $\ell$, contro la definizione di supremo come minimo dei maggioranti. Quindi

$$
\forall\varepsilon>0\quad\exists n_0\in\mathbb N:
\qquad\ell-\varepsilon<a_{n_0}\leq\ell.
\tag{2}
$$

> [!note] Il ruolo di $n_0$
> Il primo termine è $a_0$. Qui, invece, $a_{n_0}$ è il termine trovato grazie alla proprietà del supremo: è già sopra $\ell-\varepsilon$. L’indice $n_0$ viene scelto dopo aver fissato $\varepsilon$ e può dipendere da esso, cioè $n_0=n_0(\varepsilon)$.

Poiché $a_n$ è **crescente**, per ogni $n\geq n_0$ vale

$$
a_n\geq a_{n_0}.
\tag{3}
$$

> [!note] Uso della monotonia
> La proprietà del supremo trova **un** termine sopra $\ell-\varepsilon$; la monotonia garantisce che anche **tutti i termini successivi** restino sopra quella soglia.

Combinando (2), (3) e (1), si ottiene che per ogni $\varepsilon>0$ esiste $n_0\in\mathbb N$ tale che, per ogni $n\geq n_0$,

$$
\ell-\varepsilon<a_{n_0}\leq a_n\leq\ell.
$$

In particolare,

$$
\forall\varepsilon>0\quad\exists n_0\in\mathbb N:
\quad\forall n\geq n_0,\qquad\ell-\varepsilon<a_n\leq\ell.
$$

Per definizione di limite, la successione converge **per difetto**:

$$
\lim_{n\to+\infty}a_n=\ell^-,
\qquad\ell=\sup_{n\in\mathbb N}a_n.
$$

> [!note] Collegamento con la definizione di limite
> Da $\ell-\varepsilon<a_n\leq\ell$ segue anche $\ell-\varepsilon<a_n<\ell+\varepsilon$, cioè $|a_n-\ell|<\varepsilon$. Il simbolo $\ell^-$ indica che i termini restano sotto il limite o coincidono con esso: il valore del limite è sempre $\ell$.

![[D09 Successione Monotona e Supremo.svg|800]]

Per una successione **decrescente e limitata**, si procede in modo analogo con l’estremo inferiore. Posto $\ell=\inf_{n\in\mathbb N}a_n\in\mathbb R$, per ogni $\varepsilon>0$ esiste $n_0\in\mathbb N$ tale che

$$
\ell\leq a_n\leq a_{n_0}<\ell+\varepsilon
\qquad\forall n\geq n_0.
$$

Quindi

$$
\lim_{n\to+\infty}a_n=\ell^+,
\qquad\ell=\inf_{n\in\mathbb N}a_n,
$$

ossia la convergenza è **per eccesso**.

### 2. Successione illimitata

Si consideri inizialmente una successione **crescente e illimitata**. Poiché è crescente,

$$
a_n\geq a_0\qquad\forall n\geq0,
$$

quindi è limitata dal basso. Essendo illimitata, deve pertanto essere **illimitata dall’alto**. In particolare, nel senso esteso,

$$
\sup_{n\in\mathbb N}a_n=+\infty.
$$

Per definizione di non limitatezza superiore, ogni soglia $M>0$ viene superata da almeno un termine:

$$
\forall M>0\quad\exists n_0\in\mathbb N:
\qquad a_{n_0}>M.
$$

> [!note] Indice e valore del termine
> $n_0$ è l’indice che individua il termine; $a_{n_0}$ è il suo valore. La disuguaglianza $a_{n_0}>M$ confronta **il valore del termine** con la soglia $M$. L’indice $n_0$ viene scelto in funzione di $M$, cioè $n_0=n_0(M)$.

Per monotonia, per ogni $n\geq n_0$ vale $a_n\geq a_{n_0}$. Ne segue che

$$
\forall M>0\quad\exists n_0\in\mathbb N:
\quad\forall n\geq n_0,\qquad a_n\geq a_{n_0}>M.
$$

In particolare,

$$
\forall M>0\quad\exists n_0\in\mathbb N:
\quad\forall n\geq n_0,\qquad a_n>M.
$$

Questa è la definizione di limite uguale a $+\infty$. Pertanto

$$
\lim_{n\to+\infty}a_n=+\infty,
\qquad\sup_{n\in\mathbb N}a_n=+\infty.
$$

> [!note] Uso della monotonia nel caso illimitato
> La non limitatezza assicura l’esistenza di **un** termine sopra ogni soglia $M$. La monotonia garantisce che anche **tutti i termini successivi** restino sopra quella soglia: questo permette di concludere che il limite è $+\infty$.

Per una successione **decrescente e illimitata**, si ha $a_n\leq a_0$ per ogni $n\in\mathbb N$: la successione è limitata dall’alto e deve quindi essere illimitata dal basso. Per ogni $M>0$ esiste $n_0\in\mathbb N$ tale che $a_{n_0}<-M$; per monotonia,

$$
a_n\leq a_{n_0}<-M\qquad\forall n\geq n_0.
$$

Quindi

$$
\lim_{n\to+\infty}a_n=-\infty,
\qquad\inf_{n\in\mathbb N}a_n=-\infty.
$$

## Il viceversa non vale

Il teorema afferma che una successione monotona è regolare. Il viceversa è falso: una successione può ammettere limite senza essere monotona.

Per esempio, per $n\geq1$,

$$
a_n=\frac{(-1)^n}{n}
$$

converge a $0$, poiché $|a_n|=1/n\to0$, ma non è monotona: $a_1=-1<a_2=1/2$ e $a_2=1/2>a_3=-1/3$.

## Da ricordare

**Regolare** comprende anche i limiti infiniti. Monotona non significa necessariamente convergente a un numero finito: per esempio $a_n=n$ tende a $+\infty$.

## Note di riferimento

[[76 Teorema del Limite delle Successioni Monotone]]
