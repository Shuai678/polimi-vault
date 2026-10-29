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

# Enunciati — Serie Numeriche

[[00 Dimostrazioni Prima Prova in Itinere|Indice di teoremi e dimostrazioni]] · [[00 Indice Formulario|Formulario]]

Le prove richieste sulle serie sono [[D10 Condizione Necessaria di Convergenza di una Serie]], [[D11 Teorema del Confronto per le Serie]], [[D12 Teorema del Confronto Asintotico per le Serie]], [[D13 Criterio del Rapporto per le Serie Numeriche]] e [[D14 Convergenza Assoluta Implica Convergenza Semplice]]. Qui sono raccolti gli altri enunciati e le serie campione.

## 1. Definizioni indispensabili

Per una serie $\sum_{n=n_0}^{\infty}a_n$, la successione delle somme parziali è

$$
S_N=\sum_{n=n_0}^{N}a_n.
$$

La serie converge se $S_N$ tende a un numero reale; diverge a $+\infty$ o $-\infty$ se ha quel limite infinito; è irregolare se $S_N$ non ha limite nella retta reale estesa.

La convergenza **semplice** è questa normale convergenza. La convergenza **assoluta** è la convergenza di $\sum|a_n|$. Una serie convergente ma non assolutamente è **solo semplicemente**, o **condizionatamente**, convergente.

Riferimenti: [[99 Serie Numeriche e Somme Parziali]] e [[114 Convergenza Assoluta e Semplice delle Serie]].

## 2. Serie geometrica

Per $q\neq1$ e $N\geq0$,

$$
\sum_{n=0}^{N}q^n=\frac{1-q^{N+1}}{1-q}.
$$

La serie $\sum_{n=0}^{\infty}q^n$ ha il seguente carattere:

| Ragione | Risultato |
| --- | --- |
| $\lvert q\rvert<1$ | Converge, con somma $1/(1-q)$ |
| $q\geq1$ | Diverge a $+\infty$ |
| $q\leq-1$ | È irregolare |

Se $|q|<1$, partendo da $n=1$ la somma è $q/(1-q)$. Il resto dopo l’indice $N$ è $q^{N+1}/(1-q)$.

Riferimento: [[100 Serie Geometrica e Rappresentazioni Decimali]].

## 3. Linearità, code e resto

Se $\sum a_n=A$ e $\sum b_n=B$ sono convergenti e $\alpha,\beta\in\mathbb R$, allora

$$
\sum(\alpha a_n+\beta b_n)=\alpha A+\beta B.
$$

Cambiare o togliere un numero finito di termini **non cambia il carattere**. Può cambiare il valore della somma. Per serie regolari si possono usare le regole dei limiti estesi soltanto quando non compare una forma indeterminata.

Se $\sum a_n=S\in\mathbb R$, il resto è

$$
R_N=\sum_{n=N+1}^{\infty}a_n=S-S_N\longrightarrow0.
$$

Riferimenti: [[101 Linearità e Algebra delle Serie]] e [[105 Code e Resto di una Serie]].

## 4. Serie telescopiche

Se $a_n=b_n-b_{n+1}$, per ogni somma finita

$$
\sum_{n=m}^{N}a_n=b_m-b_{N+1}.
$$

In particolare, se $b_n\to b\in\mathbb R$, la serie converge e la somma è $b_m-b$. Viceversa, la convergenza della serie impone che $b_n$ abbia limite finito, per la stessa identità.

La serie di Mengoli soddisfa

$$
\sum_{n=1}^{\infty}\frac1{n(n+1)}=1,
\qquad R_N=\frac1{N+1}.
$$

Riferimento: [[102 Serie Telescopiche e Serie di Mengoli]].

## 5. Regolarità delle serie a termini non negativi

Se $a_n\geq0$ definitivamente, la serie è regolare: converge a un numero reale oppure diverge a $+\infty$. Non può essere irregolare o divergere a $-\infty$.

Converge **se e solo se** le somme parziali sono limitate superiormente. Quando la positività vale soltanto nella coda, si applica il teorema alla coda e poi si aggiungono i primi termini.

La condizione $a_n\to0$ resta soltanto necessaria: vedi [[D10 Condizione Necessaria di Convergenza di una Serie]]. Per i confronti: [[D11 Teorema del Confronto per le Serie]] e [[D12 Teorema del Confronto Asintotico per le Serie]].

Riferimento: [[106 Serie a Termini Positivi]].

## 6. Serie armoniche generalizzate e di Bertrand

Per ogni $\alpha\in\mathbb R$,

$$
\sum_{n=1}^{\infty}\frac1{n^\alpha}
\quad\text{converge se e solo se}\quad\alpha>1.
$$

Negli altri casi diverge a $+\infty$. In particolare la serie armonica, $\alpha=1$, diverge.

Per $\alpha,\beta\in\mathbb R$, con $\log=\ln$,

$$
\sum_{n=2}^{\infty}\frac1{n^\alpha(\log n)^\beta}
$$

converge se e solo se

$$
\alpha>1\quad\text{oppure}\quad\alpha=1\text{ e }\beta>1.
$$

Diverge a $+\infty$ in tutti gli altri casi. Le classificazioni sono da conoscere e usare; non sono nuove dimostrazioni D dell’elenco dello scritto.

Riferimenti: [[104 Serie Armonica]] e [[108 Serie Armoniche Generalizzate e di Bertrand]].

## 7. Criterio della radice

Sia $a_n\geq0$ definitivamente e supponiamo che esista

$$
\ell=\lim_{n\to\infty}\sqrt[n]{a_n}\in[0,+\infty].
$$

- Se $\ell<1$, $\sum a_n$ converge e $a_n\to0$.
- Se $\ell>1$, incluso $+\infty$, $\sum a_n$ diverge a $+\infty$ e $a_n\to+\infty$.
- Se $\ell=1$, il criterio non decide.

La radice ammette termini nulli; il rapporto richiede denominatori non nulli nella coda. Il rapporto è nella scheda [[D13 Criterio del Rapporto per le Serie Numeriche]].

Riferimento: [[111 Criterio della Radice per Serie]].

## 8. Formula di Stirling

Per $n\to+\infty$ lungo gli interi positivi,

$$
n!\sim\sqrt{2\pi n}\left(\frac ne\right)^n.
$$

Si tratta di un’equivalenza, non di un’uguaglianza esatta. Per esempio

$$
\frac{n!}{n^n}\sim\frac{\sqrt{2\pi n}}{e^n}.
$$

Riferimento: [[112 Formula di Stirling e Serie con Fattoriali]].

## 9. Convergenza assoluta e disuguaglianza per la somma

L’enunciato e la prova sono in [[D14 Convergenza Assoluta Implica Convergenza Semplice]]:

$$
\sum|a_n|<+\infty\Longrightarrow\sum a_n\in\mathbb R,
\qquad
\left|\sum a_n\right|\leq\sum|a_n|.
$$

Il viceversa è falso. Se $a_n\geq0$ definitivamente, convergenza semplice e assoluta coincidono, poiché le code della serie originale e di quella dei moduli sono uguali.

Riferimento: [[114 Convergenza Assoluta e Semplice delle Serie]].

## 10. Criterio di Leibniz e stima del resto

Consideriamo $\sum_{n=0}^{\infty}(-1)^n a_n$. Supponiamo che, definitivamente, $a_n\geq0$, $a_{n+1}\leq a_n$ e $a_n\to0$.

Allora la serie converge a $S\in\mathbb R$. Se $S_N=\sum_{n=0}^{N}(-1)^n a_n$, per $N$ sufficientemente grande

$$
|S-S_N|\leq a_{N+1},\qquad
(-1)^{N+1}(S-S_N)\geq0.
$$

L’errore è quindi al più la grandezza del primo termine escluso e ne ha il segno, quando è non nullo. Se le ipotesi valgono dall’inizio, la stima vale per ogni indice. Le somme parziali pari si avvicinano dall’alto e quelle dispari dal basso, da una soglia in poi.

Leibniz prova la convergenza: per stabilire se è assoluta occorre studiare separatamente la serie dei moduli. La sua dimostrazione non è tra D1–D14; nel PDF il docente indica «NO DIM.».

Riferimento: [[115 Serie Alternate e Criterio di Leibniz]].

## 11. Armoniche alternate e cautele sull’equivalenza

Per la serie $\sum_{n=1}^{\infty}(-1)^n/n^\alpha$:

| Esponente | Carattere |
| --- | --- |
| $\alpha>1$ | Assolutamente convergente |
| $0<\alpha\leq1$ | Convergente solo semplicemente |
| $\alpha\leq0$ | Irregolare |

La sola alternanza dei segni e il limite zero dei termini non sostituiscono la verifica della monotonia richiesta da Leibniz. Inoltre, ampiezze equivalenti non garantiscono lo stesso carattere delle serie alternate.

Riferimenti: [[115 Serie Alternate e Criterio di Leibniz]] e [[116 Monotonia e Confronti nelle Serie Alternate]]. Per le famiglie parametriche svolte dal docente: [[113 Serie con Fattori Esponenziali Potenze e Logaritmi]] e [[117 Discussione Parametrica delle Serie a Segno Variabile]]. Per gli equivalenti con esponente variabile: [[118 Equivalenti con Esponente Variabile nelle Serie]] e [[Enunciati 03 Equivalenti e Limiti Notevoli#6. Forma esponenziale generale]].
