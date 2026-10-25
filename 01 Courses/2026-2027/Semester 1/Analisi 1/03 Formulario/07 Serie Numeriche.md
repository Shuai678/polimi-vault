---
course: Analisi 1
type: formula-sheet
updated: 2026-10-25
---

# Serie numeriche

[[03 Formulario|Indice del formulario]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map/00 Course Map|Corso]]

> [!note] Integrazioni della Lezione 12 — Da studiare
> Convergenza assoluta e D14, Leibniz, cautele sulle alternate ed esponente variabile sono preparati per lo studio successivo.

| Voce | Essenziale |
| --- | --- |
| [[99 Serie Numeriche e Somme Parziali\|Serie e somme parziali]] | $S_N=\sum_{n=n_0}^{N}a_n$. $\sum a_n$ converge se $S_N\to S\in\mathbb R$; diverge se $S_N\to\pm\infty$; è irregolare se il limite non esiste nei reali estesi. |
| [[103 Condizione Necessaria di Convergenza di una Serie\|Condizione necessaria]] **D10** | $\sum a_n$ convergente $\Rightarrow a_n\to0$; usare $a_N=S_N-S_{N-1}$. Il viceversa è falso: la serie armonica diverge. |
| [[100 Serie Geometrica e Rappresentazioni Decimali\|Serie geometrica]] | $\sum_{n=0}^{N}q^n=(1-q^{N+1})/(1-q)$ per $q\neq1$. $\sum_{n=0}^{\infty}q^n$ converge esattamente per $\lvert q\rvert<1$, con somma $1/(1-q)$; da $n=1$ la somma è $q/(1-q)$. |
| [[102 Serie Telescopiche e Serie di Mengoli\|Telescopiche e Mengoli]] | Se $a_n=b_n-b_{n+1}$, $\sum_{n=m}^{N}a_n=b_m-b_{N+1}$. Se $b_n\to b\in\mathbb R$, la somma è $b_m-b$. $\sum_{n=1}^{\infty}1/[n(n+1)]=1$. |
| [[101 Linearità e Algebra delle Serie\|Linearità]] · [[105 Code e Resto di una Serie\|resto]] | Per serie convergenti: $\sum(\alpha a_n+\beta b_n)=\alpha\sum a_n+\beta\sum b_n$. $R_N=\sum_{n=N+1}^{\infty}a_n=S-S_N\to0$. Cambiare finiti termini conserva il carattere, non necessariamente la somma. |
| [[106 Serie a Termini Positivi\|Termini non negativi]] | Se $a_n\geq0$ definitivamente, la serie converge o diverge a $+\infty$. Converge se e solo se le somme parziali sono limitate superiormente. |
| [[107 Criterio del Confronto per Serie\|Confronto]] **D11** | $0\leq a_n\leq b_n$ definitivamente: $\sum b_n$ convergente $\Rightarrow\sum a_n$ convergente; $\sum a_n=+\infty\Rightarrow\sum b_n=+\infty$. |
| [[109 Criterio del Confronto Asintotico per Serie\|Confronto asintotico]] **D12** | $a_n,b_n>0$ definitivamente e $a_n/b_n\to1\Rightarrow$ stesso carattere delle due serie. |
| [[110 Criterio del Rapporto per Serie\|Rapporto per serie]] **D13** | $a_n>0$ definitivamente, $L=\lim a_{n+1}/a_n\in[0,+\infty]$: $L<1$ converge; $L>1$ diverge a $+\infty$; $L=1$ non decide. |
| [[111 Criterio della Radice per Serie\|Radice per serie]] | $a_n\geq0$ definitivamente, $L=\lim\sqrt[n]{a_n}\in[0,+\infty]$: $L<1$ converge; $L>1$ diverge a $+\infty$; $L=1$ non decide. |
| [[104 Serie Armonica\|Armonica]] · [[108 Serie Armoniche Generalizzate e di Bertrand\|armoniche generalizzate]] | $\sum_{n=1}^{\infty}1/n=+\infty$. $\sum_{n=1}^{\infty}1/n^\alpha$ converge se e solo se $\alpha>1$. |
| [[108 Serie Armoniche Generalizzate e di Bertrand\|Serie di Bertrand]] | $\sum_{n=2}^{\infty}1/[n^\alpha(\log n)^\beta]$ converge se $\alpha>1$ oppure $\alpha=1$, $\beta>1$; diverge negli altri casi. |
| [[112 Formula di Stirling e Serie con Fattoriali\|Stirling]] | $n!\sim\sqrt{2\pi n}(n/e)^n$; quindi $n!/n^n\sim\sqrt{2\pi n}/e^n$. |
| [[114 Convergenza Assoluta e Semplice delle Serie\|Convergenza assoluta ⇒ semplice]] **D14** | $\sum\lvert a_n\rvert<+\infty\Rightarrow\sum a_n\in\mathbb R$, con $\lvert\sum a_n\rvert\leq\sum\lvert a_n\rvert$. Prova: $0\leq a_n+\lvert a_n\rvert\leq2\lvert a_n\rvert$, confronto e differenza di due serie convergenti. Il viceversa è falso. |
| [[115 Serie Alternate e Criterio di Leibniz\|Leibniz e resto]] | $\sum(-1)^n a_n$: se $a_n\geq0$, $a_{n+1}\leq a_n$ definitivamente e $a_n\to0$, converge; $\lvert S-S_N\rvert\leq a_{N+1}$ per $N$ nella coda valida. Ipotesi globali ⇒ stima per ogni indice. |
| [[114 Convergenza Assoluta e Semplice delle Serie\|Solo semplice]] · [[115 Serie Alternate e Criterio di Leibniz\|armonica alternata]] | Solo semplice = serie convergente e serie dei moduli divergente. $\sum(-1)^n/n^\alpha$: assoluta per $\alpha>1$; solo semplice per $0<\alpha\leq1$; irregolare per $\alpha\leq0$. |
| [[116 Monotonia e Confronti nelle Serie Alternate\|Monotonia ed equivalenze]] | Ampiezze positive equivalenti non garantiscono uguale carattere delle serie alternate né monotonia dell'ampiezza. La monotonia definitiva di Leibniz va verificata. |
| [[118 Equivalenti con Esponente Variabile nelle Serie\|Potenza con esponente variabile]] | $(1+\varepsilon_n)^{c_n}-1\sim c_n\varepsilon_n$: richiede $\varepsilon_n\to0$, $c_n\varepsilon_n\to0$, base positiva e fattori non nulli definitivamente. Scrivere $e^{c_n\log(1+\varepsilon_n)}-1$ e controllare che l'esponente tenda a zero. |

[[03 Formulario#Indice rapido|↑ Indice]]
