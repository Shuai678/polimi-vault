---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-11-03
source:
  - "Lezione 13, PDF pp. 3-11, stampate 110-118"
  - "Esempi aggiuntivi del tutor, indicati nelle sezioni"
---

# Combinazioni, generatori, indipendenza e basi

Stato: **da studiare**. Gli svolgimenti sono del tutor e non attestano esercizi completati dallo studente. I riquadri delle soluzioni sono richiudibili per consentire un successivo allenamento.

## 1 Quattro generatori di tre coordinate

**Fonte:** Lezione 13, pp. 5-6. Determinare se i vettori seguenti generano $\mathbb R^3$ e descrivere tutte le rappresentazioni di $(a,b,c)^{\mathsf T}$:

$$
v_1=(1,0,0)^{\mathsf T},\quad
v_2=(-2,1,0)^{\mathsf T},\quad
v_3=(0,1,1)^{\mathsf T},\quad
v_4=(1,-1,2)^{\mathsf T}.
$$

> [!example]- Svolgimento completo
> Mettiamo i vettori per colonne e i coefficienti della combinazione come incognite:
>
> $$
> \begin{bmatrix}
> 1&-2&0&1&a\\
> 0&1&1&-1&b\\
> 0&0&1&2&c
> \end{bmatrix}.
> $$
>
> La matrice dei coefficienti è già a scala con tre pivot, quindi il sistema è compatibile per ogni $(a,b,c)$.
>
> La quarta variabile è libera: poniamo $\lambda_4=t$. Dalla terza riga:
>
> $$
> \lambda_3+2t=c\implies\lambda_3=c-2t.
> $$
>
> Dalla seconda:
>
> $$
> \lambda_2+\lambda_3-t=b
> \implies\lambda_2=b-c+3t.
> $$
>
> Dalla prima:
>
> $$
> \lambda_1-2\lambda_2+t=a
> \implies\lambda_1=a+2b-2c+5t.
> $$
>
> Tutte le rappresentazioni sono quindi
>
> $$
> \lambda=
> \begin{pmatrix}a+2b-2c\\b-c\\c\\0\end{pmatrix}
> +t\begin{pmatrix}5\\3\\-2\\1\end{pmatrix}.
> $$
>
> Controllo delle coordinate:
>
> $$
> \lambda_1-2\lambda_2+\lambda_4=a,\quad
> \lambda_2+\lambda_3-\lambda_4=b,\quad
> \lambda_3+2\lambda_4=c.
> $$
>
> Il rango massimo prova che i vettori sono generatori; il parametro libero mostra che non sono indipendenti.

## 2 Trovare la relazione ed estrarre una base

**Fonte:** Lezione 13, pp. 7-10; stessi vettori dell'esempio 1. Trovare una relazione non banale ed eliminare un vettore senza perdere lo span.

> [!example]- Relazione, eliminazione e verifica
> Ponendo $a=b=c=0$ nella formula precedente:
>
> $$
> \lambda=t(5,3,-2,1)^{\mathsf T}.
> $$
>
> Con $t=1$ otteniamo $5v_1+3v_2-2v_3+v_4=0$, dunque
>
> $$
> v_4=-5v_1-3v_2+2v_3.
> $$
>
> Si può scartare $v_4$. Le tre colonne rimaste formano la matrice
>
> $$
> A_0=\begin{pmatrix}1&-2&0\\0&1&1\\0&0&1\end{pmatrix}.
> $$
>
> È triangolare con tre pivot non nulli. Genera $\mathbb R^3$ e il suo sistema omogeneo ha soltanto la soluzione nulla. Quindi $(v_1,v_2,v_3)$ è una base.
>
> La relazione non impone che si debba eliminare proprio $v_4$: si può isolare qualsiasi vettore con coefficiente non nullo. La scelta qui conserva i primi tre, già triangolari.

## 3 Due rappresentazioni diventano le stesse coordinate

**Fonte:** Lezione 13, pp. 6 e 9. Per $u=(0,1,3)^{\mathsf T}$ verificare le due rappresentazioni del professore e trovare le coordinate nella base $(v_1,v_2,v_3)$.

> [!example]- Confronto delle rappresentazioni
> Le due liste sono $(1,1,1,1)$ e $(6,4,-1,2)$.
>
> $$
> v_1+v_2+v_3+v_4=(1-2+0+1,\ 0+1+1-1,\ 0+0+1+2)=(0,1,3),
> $$
>
> $$
> 6v_1+4v_2-v_3+2v_4
> =(6-8+2,\ 4-1-2,\ -1+4)=(0,1,3).
> $$
>
> Sostituiamo $v_4=-5v_1-3v_2+2v_3$.
>
> Nella prima espressione i coefficienti diventano
>
> $$
> (1-5,\ 1-3,\ 1+2)=(-4,-2,3).
> $$
>
> Nella seconda:
>
> $$
> (6-10,\ 4-6,\ -1+4)=(-4,-2,3).
> $$
>
> Quindi $[u]_{\mathcal B}=(-4,-2,3)^{\mathsf T}$. Le coordinate sono uniche nella base, non nella famiglia ridondante di quattro generatori.

## 4 Polinomi come vettori

**Fonte:** esempio del tutor, collegato ai monomi delle pp. 3-4. In $\mathbb R[t]_{\le2}$ stabilire se $(1+t,1-t,t^2)$ è una base e rappresentare $p(t)=2+3t-t^2$.

> [!example]- Confronto dei coefficienti
> Una combinazione ha la forma
>
> $$
> \alpha(1+t)+\beta(1-t)+\gamma t^2
> =(\alpha+\beta)+(\alpha-\beta)t+\gamma t^2.
> $$
>
> Se è il polinomio nullo, $\alpha+\beta=0$, $\alpha-\beta=0$, $\gamma=0$, quindi tutti i coefficienti sono nulli. La famiglia è indipendente.
>
> Per un polinomio arbitrario $a+bt+ct^2$ si risolve
>
> $$
> \alpha=\frac{a+b}{2},\quad
> \beta=\frac{a-b}{2},\quad \gamma=c.
> $$
>
> La famiglia genera e dunque è una base. Per il polinomio assegnato:
>
> $$
> p=\frac52(1+t)-\frac12(1-t)-t^2.
> $$
>
> Verifica: il termine costante è $5/2-1/2=2$, quello lineare è $5/2+1/2=3$, quello quadratico è $-1$.
>
> Il calcolo è su $\mathbb R$: su $\mathbb F_2$ i primi due polinomi coinciderebbero.

## 5 Non confondere le due proprietà

**Fonte:** confronto aggiuntivo del tutor.

- In $\mathbb R^3$, $(e_1,e_2)$ è indipendente ma non genera, perché ogni combinazione ha terza coordinata zero.
- I quattro vettori dell'esempio 1 generano ma sono dipendenti.
- Una base richiede entrambe le proprietà; non è sufficiente che i vettori siano semplicemente distinti.

## Teoria e fonte

- [[42 Combinazioni Lineari e Span]], [[43 Generatori e Sistemi Lineari]], [[44 Dipendenza e Indipendenza Lineare]], [[45 Basi e Unicità delle Coordinate]].
- [[GAL 2026-2027 - 20261019 - LEZIONE 13.pdf#page=3|Lezione 13, pp. 3-11, stampate 110-118]].
