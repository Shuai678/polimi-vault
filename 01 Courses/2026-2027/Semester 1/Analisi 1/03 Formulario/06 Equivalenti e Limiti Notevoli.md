---
course: Analisi 1
type: formula-sheet
updated: 2026-10-24
---

# Equivalenti e limiti notevoli

[[03 Formulario|Indice del formulario]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map/00 Course Map|Corso]]

Per i rapporti si richiede denominatore non nullo definitivamente; gli angoli sono in radianti. In questa sezione $t=t_n\to0$, $t_n\neq0$ definitivamente.

| Voce | Essenziale |
| --- | --- |
| [[93 Notazione o-Piccolo\|o-piccolo]] · [[94 Equivalenza Asintotica\|equivalenza]] | $a_n=o(b_n)\iff a_n/b_n\to0$. $a_n\sim b_n\iff a_n/b_n\to1\iff a_n=b_n+o(b_n)$. Equivalenza significa errore relativo nullo. |
| [[90 Numero di Nepero e Limiti di Tipo Esponenziale\|Numero di Nepero]] | $e=\lim_{n\to\infty}(1+1/n)^n$; $(1+a/n)^n\to e^a$ per $a\in\mathbb R$ fissato. Più in generale $(1+1/c_n)^{c_n}\to e$ se $c_n\to\pm\infty$. |
| [[95 Equivalenti e Sviluppi Asintotici Notevoli\|Seno e arcotangente]] | $\sin t\sim t$; $\arctan t\sim t$. Quindi $\sin t/t\to1$ e $\arctan t/t\to1$. |
| [[95 Equivalenti e Sviluppi Asintotici Notevoli\|Coseno]] | $1-\cos t\sim t^2/2$; $\cos t=1-t^2/2+o(t^2)$. |
| [[95 Equivalenti e Sviluppi Asintotici Notevoli\|Esponenziale e logaritmo]] | $e^t-1\sim t$; $\log(1+t)\sim t$. Equivalentemente $e^t=1+t+o(t)$ e $\log(1+t)=t+o(t)$. |
| [[95 Equivalenti e Sviluppi Asintotici Notevoli\|Potenza con incremento piccolo]] | $(1+t)^\alpha-1\sim\alpha t$ per $\alpha\neq0$ fissato; $(1+t)^\alpha=1+\alpha t+o(t)$. La base è positiva definitivamente. |
| [[85 Gerarchia degli Infiniti\|Gerarchia degli infiniti]] | $(\log_a n)^\beta=o(n^\alpha)$, $n^\alpha=o(a^n)$, $a^n=o(n!)$, $n!=o(n^n)$; $a>1$, $\alpha,\beta>0$ fissati. |
| [[86 Termine Dominante nei Rapporti di Successioni\|Termini dominanti]] | Se $P_n\sim An^p$, $Q_n\sim Bn^q$, $A,B\neq0$, allora $P_n/Q_n\sim(A/B)n^{p-q}$. |
| [[88 Razionalizzazione e Differenze di Radicali\|Razionalizzazione]] · [[97 Cancellazioni e Precisione del Resto Asintotico\|cancellazioni]] | $\sqrt A-\sqrt B=(A-B)/(\sqrt A+\sqrt B)$ per $A,B\geq0$, non entrambi nulli. Nelle differenze gli equivalenti dei singoli termini possono non bastare: conservare i resti alla scala necessaria. |
| [[96 Calcolo dei Limiti con Equivalenti Asintotici\|Calcolo con equivalenti]] · [[98 Equivalenti Asintotici nelle Funzioni Composte\|composizioni]] | Sostituire in prodotti e quozienti verificando i domini; nelle composizioni controllare ogni argomento. Somme, differenze e potenze variabili richiedono un controllo ulteriore. |

[[03 Formulario#Indice rapido|↑ Indice]]
