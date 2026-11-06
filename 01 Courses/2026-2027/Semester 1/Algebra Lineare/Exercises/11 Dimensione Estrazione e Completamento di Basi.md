---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-11-03
source:
  - "Lezione 15, PDF pp. 2-11, stampate 120-129"
  - "Esempi aggiuntivi del tutor, indicati nelle sezioni"
---

# Dimensione, estrazione e completamento di basi

Stato: **da studiare**. Gli svolgimenti sono del tutor e non attestano esercizi completati dallo studente. I riquadri delle soluzioni sono richiudibili per consentire un successivo allenamento.

## 1 Costruire una base mediante le righe

**Fonte:** Lezione 15, pp. 8-9.

$$
V=\operatorname{Span}\big((1,-1,0),(0,1,2),(1,0,2)\big).
$$

Costruire una base di $V$ e determinarne la dimensione.

> [!example]- Operazioni e interpretazione
> Mettiamo i vettori per righe:
>
> $$
> A=\begin{pmatrix}1&-1&0\\0&1&2\\1&0&2\end{pmatrix}
> \xrightarrow{R_3\leftarrow R_3-R_1}
> \begin{pmatrix}1&-1&0\\0&1&2\\0&1&2\end{pmatrix}
> \xrightarrow{R_3\leftarrow R_3-R_2}
> \begin{pmatrix}1&-1&0\\0&1&2\\0&0&0\end{pmatrix}.
> $$
>
> Le righe non nulle finali sono indipendenti e generano lo stesso spazio:
>
> $$
> \mathcal B=((1,-1,0),(0,1,2)),\qquad \dim V=2.
> $$
>
> In questo esempio coincidono con due righe iniziali. In generale le righe trasformate possono essere diverse da tutti i vettori di partenza: il metodo costruisce una base, ma non garantisce l'estrazione.
>
> Si vede anche direttamente che $(1,0,2)=(1,-1,0)+(0,1,2)$.

## 2 Estrarre colonne originali

**Fonte:** Lezione 15, pp. 9-11.

$$
w_1=(0,2,1)^{\mathsf T},\quad
w_2=(4,1,2)^{\mathsf T},\quad
w_3=(4,-3,0)^{\mathsf T}.
$$

Estrarre una base di $W=\operatorname{Span}(w_1,w_2,w_3)$ senza sostituire i vettori selezionati con combinazioni nuove.

> [!example]- Gauss, indici pivot e relazione
> Mettiamo i vettori per colonne:
>
> $$
> A=\begin{pmatrix}0&4&4\\2&1&-3\\1&2&0\end{pmatrix}.
> $$
>
> Scambiamo $R_1,R_3$ per usare il pivot 1:
>
> $$
> \begin{pmatrix}1&2&0\\2&1&-3\\0&4&4\end{pmatrix}
> \xrightarrow{R_2\leftarrow R_2-2R_1}
> \begin{pmatrix}1&2&0\\0&-3&-3\\0&4&4\end{pmatrix}.
> $$
>
> Normalizziamo il secondo pivot:
>
> $$
> R_2\leftarrow-\frac13R_2:
> \qquad
> \begin{pmatrix}1&2&0\\0&1&1\\0&4&4\end{pmatrix}.
> $$
>
> Infine $R_3\leftarrow R_3-4R_2$:
>
> $$
> U=\begin{pmatrix}1&2&0\\0&1&1\\0&0&0\end{pmatrix}.
> $$
>
> I pivot sono nelle colonne 1 e 2. Si conservano le colonne 1 e 2 di **$A$**:
>
> $$
> \mathcal B=(w_1,w_2),\qquad\dim W=2.
> $$
>
> Dall'omogeneo $U\lambda=0$:
>
> $$
> \lambda_3=t,\quad\lambda_2=-t,\quad\lambda_1=2t.
> $$
>
> Quindi $2w_1-w_2+w_3=0$ e $w_3=w_2-2w_1$.
>
> Controllo: $(4,1,2)-2(0,2,1)=(4,-3,0)$.
>
> Le colonne pivot di $U$, $(1,0,0)^{\mathsf T}$ e $(2,1,0)^{\mathsf T}$, generano un altro piano: non sono una risposta valida alla richiesta di estrarre i vettori originali.

## 3 Confrontare costruzione ed estrazione sullo stesso esempio

**Fonte:** Lezione 15, p. 9, vettori dell'esempio 2 disposti per righe.

> [!example]- Base nuova dallo span delle righe
> $$
> A_R=
> \begin{pmatrix}0&2&1\\4&1&2\\4&-3&0\end{pmatrix}
> \xrightarrow{R_1\leftrightarrow R_2}
> \begin{pmatrix}4&1&2\\0&2&1\\4&-3&0\end{pmatrix}.
> $$
>
> Con $R_3\leftarrow R_3-R_1$ si ha $R_3=(0,-4,-2)$. Con $R_3\leftarrow R_3+2R_2$ si ottiene la riga nulla:
>
> $$
> \begin{pmatrix}4&1&2\\0&2&1\\0&0&0\end{pmatrix}.
> $$
>
> Le righe non nulle danno la base $((4,1,2),(0,2,1))$. Anche qui sono vettori iniziali, ma per una circostanza favorevole dell'esempio.
>
> Se riscalassimo la prima riga dividendo per 4, avremmo una base altrettanto valida dello span, ma contenente $(1,1/4,1/2)$, che non era un vettore iniziale. Ecco perché si distingue «costruire» da «estrarre».

## 4 Completare due vettori a una base

**Fonte:** Lezione 15, p. 11.

$$
v_1=(1,0,1)^{\mathsf T},\qquad v_2=(0,1,1)^{\mathsf T}.
$$

Completare la famiglia a una base di $\mathbb R^3$.

> [!example]- Aggiungere i canonici e conservarne uno
> Si affiancano i canonici dopo i vettori da conservare:
>
> $$
> \begin{pmatrix}1&0&1&0&0\\0&1&0&1&0\\1&1&0&0&1\end{pmatrix}
> \xrightarrow{R_3\leftarrow R_3-R_1}
> \begin{pmatrix}1&0&1&0&0\\0&1&0&1&0\\0&1&-1&0&1\end{pmatrix}
> $$
>
> $$
> \xrightarrow{R_3\leftarrow R_3-R_2}
> \begin{pmatrix}1&0&1&0&0\\0&1&0&1&0\\0&0&-1&-1&1\end{pmatrix}.
> $$
>
> I pivot sono nelle colonne 1, 2 e 3, quindi la base estratta dalla matrice iniziale è $(v_1,v_2,e_1)$.
>
> Il piano iniziale è $z=x+y$; $e_1=(1,0,0)$ non vi appartiene. Per ogni $(x,y,z)$:
>
> $$
> (x,y,z)=(z-y)v_1+yv_2+(x-z+y)e_1.
> $$
>
> Le tre coordinate determinano univocamente i coefficienti.

## 5 Numeri di vettori e dimensione

**Fonte:** applicazioni del tutor al lemma fondamentale.

> [!example]- Quattro conclusioni con le rispettive ipotesi
> 1. Cinque vettori in $M_{\mathbb R}(2,2)$ sono dipendenti, perché la dimensione è 4.
> 2. Tre polinomi in $\mathbb R[t]_{\le3}$ non possono generare tutto lo spazio: la dimensione è 4.
> 3. Quattro matrici indipendenti di $M_{\mathbb R}(2,2)$ sono automaticamente una base.
> 4. Tre generatori di un piano vettoriale possono essere dipendenti; per estrarre una base se ne conservano due indipendenti.
>
> Le conclusioni automatiche richiedono che l'ambiente e la sua dimensione siano già noti.

## Fac-simile allegato alla stessa lezione

Il problema su $BA=0$, basi di sottospazi di matrici e decomposizione dell'identità è archiviato in [[01 Fac-simile Matrici e Sottospazi del 28 ottobre 2026]], nella sezione delle prove. Non è una simulazione svolta dallo studente.

## Teoria e fonte

- [[46 Lemma Fondamentale e Teorema della Dimensione]], [[47 Basi Canoniche e Spazi Finitamente Generati]], [[48 Estrazione di una Base con Gauss]], [[49 Completamento di Vettori Indipendenti a una Base]].
- [[GAL 2026-2027 - 20261028 - LEZIONE 15.pdf#page=2|Lezione 15, pp. 2-11, stampate 120-129]].
