---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-11-03
source:
  - "Lezione 13, PDF pp. 7-10, stampate 114-117"
---

# Dipendenza e indipendenza lineare

Stato: **da studiare**.

## Quale problema risolve la definizione

I generatori permettono di rappresentare i vettori. L'indipendenza lineare impedisce che due diverse scelte di coefficienti rappresentino lo stesso vettore dello span.

Per controllarla basta studiare le rappresentazioni dello **zero**.

## Definizione 13.3

I vettori $v_1,\ldots,v_s$ sono linearmente indipendenti se

$$
\boxed{\lambda_1v_1+\cdots+\lambda_sv_s=0
\implies \lambda_1=\cdots=\lambda_s=0.}
$$

La relazione con tutti i coefficienti nulli esiste sempre ed è detta banale. Indipendenza significa che è **l'unica** relazione che produce zero.

La famiglia è linearmente dipendente se esiste una relazione nulla con coefficienti **non tutti nulli**. Non occorre che siano tutti diversi da zero.

## Equivalenza con l'unicità nello span

Se

$$
\sum_i\lambda_iv_i=\sum_i\mu_iv_i,
$$

sottraendo e raccogliendo si ottiene

$$
\sum_i(\lambda_i-\mu_i)v_i=0.
$$

L'indipendenza impone $\lambda_i=\mu_i$ per ogni $i$.

Viceversa, se le rappresentazioni dei vettori dello span sono uniche, lo zero non può avere una rappresentazione diversa da quella banale. Quindi la famiglia è indipendente.

Questo non afferma ancora che si rappresentino tutti gli elementi di un ambiente più grande: per quello serve essere generatori.

## Come verificare con Gauss

Se i vettori sono colonne di $A:m\times s$, si risolve

$$
A\lambda=0.
$$

Il sistema omogeneo è sempre compatibile. Ha la sola soluzione nulla esattamente quando non ci sono variabili libere:

$$
\boxed{v_1,\ldots,v_s\text{ indipendenti}\iff r(A)=s.}
$$

Quindi se $s>m$ i vettori sono necessariamente dipendenti. Se $s\le m$, non si può concludere senza un controllo.

## Relazione dell'esempio del professore

Per i quattro vettori di [[43 Generatori e Sistemi Lineari]], il sistema omogeneo dà

$$
(\lambda_1,\lambda_2,\lambda_3,\lambda_4)
=t(5,3,-2,1).
$$

Con $t=1$:

$$
5v_1+3v_2-2v_3+v_4=0.
$$

La famiglia è dipendente. Isolando $v_4$:

$$
\boxed{v_4=-5v_1-3v_2+2v_3.}
$$

Si può eliminare $v_4$ senza perdere lo span. Le prime tre colonne sono indipendenti perché il sistema triangolare omogeneo

$$
\lambda_3=0,\quad\lambda_2+\lambda_3=0,\quad
\lambda_1-2\lambda_2=0
$$

impone tutti i coefficienti nulli.

## Dipendenza come ridondanza

In una relazione $\sum_i\lambda_iv_i=0$ non banale, scegliamo un indice $j$ con $\lambda_j\ne0$. Allora

$$
v_j=-\sum_{i\ne j}\frac{\lambda_i}{\lambda_j}v_i.
$$

Quindi uno dei vettori è combinazione degli altri.

Viceversa, se un vettore è combinazione degli altri, spostando tutto a un membro si ottiene una relazione nulla non banale. Si può rimuovere un vettore con coefficiente non nullo nella relazione; non uno scelto arbitrariamente.

## Casi piccoli ed errori frequenti

- Una famiglia contenente il vettore nullo è dipendente.
- Una famiglia con un solo vettore è indipendente se e solo se il vettore è non nullo.
- Due vettori sono dipendenti se uno è multiplo dell'altro, includendo i casi con zero.
- Tre vettori non sono necessariamente indipendenti soltanto perché nessuna coppia è proporzionale.

Esempio del tutor: $(1,0)$, $(0,1)$ e $(1,1)$ non sono a coppie proporzionali, ma il terzo è la somma dei primi due.

La nozione riguarda una famiglia: eventuali ripetizioni sono rilevanti. Due copie dello stesso vettore producono la relazione $v-v=0$.

## Campo finito

Una relazione non banale basta anche su $\mathbb F_2$. Non bisogna cercare «infinite soluzioni»: il sistema omogeneo deve avere **almeno una soluzione non nulla**. Il lemma fondamentale della Lezione 15 viene formulato in modo compatibile con tutti i campi.

## Da dire all'orale

> Una famiglia è indipendente se lo zero ammette soltanto la combinazione con tutti i coefficienti nulli. Una relazione non banale mostra invece che almeno un vettore è ridondante e può essere espresso mediante gli altri.

## Collegamenti e fonte

- [[45 Basi e Unicità delle Coordinate]], [[46 Lemma Fondamentale e Teorema della Dimensione]].
- [[10 Combinazioni Generatori Indipendenza e Basi]].
- [[GAL 2026-2027 - 20261019 - LEZIONE 13.pdf#page=7|Lezione 13, pp. 7-10, stampate 114-117]].
