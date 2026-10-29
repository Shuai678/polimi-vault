---
course: Analisi 1
type: exam-theorems
exam: Prima prova in itinere
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 1: enunciati, comprensione e applicazione dei teoremi"
  - "Lezioni 01-12 e note dei concetti richiamate nelle singole sezioni"
cssclasses:
  - formulario
---

# Enunciati — Equivalenti e Limiti Notevoli

[[00 Dimostrazioni Prima Prova in Itinere|Indice di teoremi e dimostrazioni]] · [[00 Indice Formulario|Formulario]]

In questa nota $\log=\ln$. Le formule riguardano successioni reali; i rapporti richiedono denominatori non nulli definitivamente. Gli angoli sono in radianti.

## 1. Numero di Nepero

La successione $s_n=(1+1/n)^n$, per $n\geq1$, è strettamente crescente e limitata superiormente. Esiste dunque il numero reale

$$
e=\lim_{n\to\infty}\left(1+\frac1n\right)^n
=\sup\left\{\left(1+\frac1n\right)^n:n\geq1\right\}.
$$

Ogni suo termine è strettamente minore di $e$.

Se $c_n\to+\infty$ oppure $c_n\to-\infty$, allora

$$
\left(1+\frac1{c_n}\right)^{c_n}\to e.
$$

La base è positiva e $c_n\neq0$ definitivamente. Per ogni $a\in\mathbb R$ fissato,

$$
\left(1+\frac an\right)^n\to e^a.
$$

Riferimento: [[90 Numero di Nepero e Limiti di Tipo Esponenziale]].

## 2. Gerarchia degli infiniti

Per $a>1$ e $\alpha,\beta>0$ fissati,

$$
(\log n)^\beta=o(n^\alpha),\qquad
n^\alpha=o(a^n),\qquad
a^n=o(n!),\qquad
n!=o(n^n).
$$

Ogni scrittura significa che il rapporto fra il primo termine e il secondo tende a zero. Invertendo i rapporti si ottiene la corrispondente gerarchia degli infinitesimi.

Riferimenti: [[85 Gerarchia degli Infiniti]] e [[92 Confronto di Infiniti e Infinitesimi]].

## 3. Equivalenza asintotica e o-piccolo

Con $b_n\neq0$ definitivamente,

$$
a_n=o(b_n)\iff\frac{a_n}{b_n}\to0,
$$

$$
a_n\sim b_n\iff\frac{a_n}{b_n}\to1
\iff a_n=b_n+o(b_n).
$$

L’equivalenza è una relazione riflessiva, simmetrica e transitiva sulle successioni definitivamente non nulle. Due successioni equivalenti hanno definitivamente lo stesso segno; se una ha limite finito o infinito, anche l’altra ha lo stesso limite.

Le regole per i resti, quando le scale sono definitivamente non nulle, includono:

$$
o(a_n)+o(a_n)=o(a_n),\qquad
b_n\,o(a_n)=o(a_nb_n),\qquad
o(a_n)o(b_n)=o(a_nb_n).
$$

Se $a_n=o(b_n)$, allora un resto $o(a_n)$ è anche $o(b_n)$, quindi $o(a_n)+o(b_n)=o(b_n)$. Se $a_n\sim b_n$, le classi $o(a_n)$ e $o(b_n)$ coincidono.

Riferimenti: [[93 Notazione o-Piccolo]] e [[94 Equivalenza Asintotica]].

## 4. Operazioni con equivalenti

Se $a_n\sim A_n$ e $b_n\sim B_n$, con le non nullità necessarie,

$$
a_nb_n\sim A_nB_n,\qquad
\frac{a_n}{b_n}\sim\frac{A_n}{B_n}.
$$

Se inoltre $a_n,A_n>0$ definitivamente e $\alpha\in\mathbb R$ è fissato, $a_n^\alpha\sim A_n^\alpha$.

**Somme e differenze richiedono controllo:** i termini principali possono cancellarsi. Per esempio $1+1/n\sim1+1/n^2$, ma sottraendo $1$ si ottengono $1/n$ e $1/n^2$, che non sono equivalenti.

Per i logaritmi: se $a_n,A_n>0$ definitivamente, $a_n\sim A_n$ e il limite comune è $\ell\in[0,+\infty]$ con $\ell\neq1$, allora $\log a_n\sim\log A_n$. Quando il limite comune è $1$, questa conclusione non è automatica.

Riferimento: [[94 Equivalenza Asintotica]].

## 5. Equivalenti e sviluppi notevoli

Sia $t_n\to0$, con $t_n\neq0$ definitivamente. Per i logaritmi e le potenze la base $1+t_n$ è positiva definitivamente.

| Espressione | Equivalente | Scrittura con resto |
| --- | --- | --- |
| $\sin t_n$ | $t_n$ | $\sin t_n=t_n+o(t_n)$ |
| $1-\cos t_n$ | $t_n^2/2$ | $\cos t_n=1-t_n^2/2+o(t_n^2)$ |
| $\log(1+t_n)$ | $t_n$ | $\log(1+t_n)=t_n+o(t_n)$ |
| $e^{t_n}-1$ | $t_n$ | $e^{t_n}=1+t_n+o(t_n)$ |
| $(1+t_n)^\alpha-1$, $\alpha\neq0$ fissato | $\alpha t_n$ | $(1+t_n)^\alpha=1+\alpha t_n+o(t_n)$ |
| $\arctan t_n$ | $t_n$ | $\arctan t_n=t_n+o(t_n)$ |

Non serve che $t_n$ abbia un segno fisso. La formula con resto della potenza vale anche per $\alpha=0$, ma l’equivalenza con $\alpha t_n$ non si scrive in quel caso.

Riferimento: [[95 Equivalenti e Sviluppi Asintotici Notevoli]].

## 6. Forma esponenziale generale

Se $t_n\to0$, $1+t_n>0$ definitivamente e $c_nt_n\to L\in\overline{\mathbb R}$, allora

$$
(1+t_n)^{c_n}\to
\begin{cases}
e^L,&L\in\mathbb R,\\
+\infty,&L=+\infty,\\
0,&L=-\infty.
\end{cases}
$$

Si usa l’identità $\exp(c_n\log(1+t_n))$ e lo sviluppo $\log(1+t_n)=t_n+o(t_n)$, con il caso $t_n=0$ trattato direttamente. Questo è un risultato ricavato dalle formule precedenti, utile nelle applicazioni; non è una nuova voce D del regolamento.

Se inoltre $c_nt_n\to0$ e $c_nt_n\neq0$ definitivamente, vale la regola più precisa

$$
(1+t_n)^{c_n}-1\sim c_nt_n.
$$

Senza il controllo del prodotto $c_nt_n$, un esponente variabile non permette di usare automaticamente gli equivalenti con esponente fissato.

Riferimenti: [[90 Numero di Nepero e Limiti di Tipo Esponenziale]], [[95 Equivalenti e Sviluppi Asintotici Notevoli]] e [[118 Equivalenti con Esponente Variabile nelle Serie]].

## 7. Termine dominante e razionalizzazione

Se $P_n\sim An^p$ e $Q_n\sim Bn^q$, con $A,B\neq0$, allora

$$
\frac{P_n}{Q_n}\sim\frac AB\,n^{p-q}.
$$

Per $A,B\geq0$ non entrambi nulli,

$$
\sqrt A-\sqrt B=\frac{A-B}{\sqrt A+\sqrt B}.
$$

Questa identità esatta permette di risolvere cancellazioni in cui i soli equivalenti dei radicali non bastano.

Riferimenti: [[86 Termine Dominante nei Rapporti di Successioni]], [[88 Razionalizzazione e Differenze di Radicali]] e [[97 Cancellazioni e Precisione del Resto Asintotico]]. Per le composizioni: [[98 Equivalenti Asintotici nelle Funzioni Composte]]. Per Stirling: [[Enunciati 04 Serie Numeriche#8. Formula di Stirling]].
