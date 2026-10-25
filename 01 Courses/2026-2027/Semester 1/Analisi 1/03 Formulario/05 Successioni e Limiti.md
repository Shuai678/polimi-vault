---
course: Analisi 1
type: formula-sheet
updated: 2026-10-24
---

# Successioni e limiti

[[03 Formulario|Indice del formulario]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map/00 Course Map|Corso]]

| Voce | Essenziale |
| --- | --- |
| [[58 Successioni di Numeri Reali\|Successione]] · [[71 Proprietà Definitivamente Vere\|definitivamente]] | Successione reale: funzione $n\mapsto a_n\in\mathbb R$, per interi $n\geq n_0$. $P(n)$ vale definitivamente se $\exists N\ \forall n\geq N:\ P(n)$. |
| [[72 Limite Finito di una Successione\|Limite finito]] | $a_n\to\ell\in\mathbb R\iff\forall\varepsilon>0\ \exists N\ \forall n\geq N:\ \lvert a_n-\ell\rvert<\varepsilon$. L'ordine dei quantificatori è essenziale. |
| [[74 Limiti Infiniti e Regolarità delle Successioni\|Limiti infiniti e regolarità]] | $a_n\to+\infty\iff\forall M>0\ \exists N\ \forall n\geq N:\ a_n>M$; per $-\infty$: $a_n<-M$. Regolare: ammette limite finito o infinito. |
| [[73 Unicità del Limite di Successione\|Unicità del limite]] **D5** | Se esiste, il limite è unico. La nota dimostra il caso finito; l'estensione ai limiti infiniti è in [[74 Limiti Infiniti e Regolarità delle Successioni\|limiti infiniti]]. |
| [[77 Limitatezza delle Successioni Convergenti\|Convergenza e limitatezza]] **D6** | $a_n\to\ell\in\mathbb R\Rightarrow(a_n)$ limitata. Il viceversa è falso: $(-1)^n$. |
| [[79 Teorema di Permanenza del Segno\|Permanenza del segno]] **D7** | Se $a_n\to\ell>0$, anche $\ell=+\infty$, allora $a_n>0$ definitivamente; analogo negativo. Se $a_n\geq0$ definitivamente e il limite esiste, $\ell\geq0$. |
| [[82 Teorema dei Due Carabinieri\|Due carabinieri]] **D8** | Se $a_n\leq b_n\leq c_n$ definitivamente e $a_n,c_n\to\ell\in\mathbb R$, allora $b_n\to\ell$. |
| [[75 Successioni Monotone\|Monotonia]] · [[76 Teorema del Limite delle Successioni Monotone\|limite monotono]] **D9** | Crescente: $a_{n+1}\geq a_n$, limite $\sup\{a_n\}$, finito se limitata superiormente, altrimenti $+\infty$. Decrescente: limite $\inf\{a_n\}$, eventualmente $-\infty$. |
| [[80 Algebra dei Limiti di Successioni\|Algebra dei limiti]] | Se $a_n\to a$, $b_n\to b$ finiti: $a_n+b_n\to a+b$, $a_nb_n\to ab$; $a_n/b_n\to a/b$ se $b\neq0$. Per $a>0$ e basi definitivamente positive: $a_n^{b_n}\to a^b$. |
| [[81 Disuguaglianze e Passaggio al Limite\|Disuguaglianze]] · [[83 Teorema del confronto per successioni divergenti\|confronto infinito]] | $a_n\leq b_n$ definitivamente e limiti esistenti $\Rightarrow\lim a_n\leq\lim b_n$. Se $a_n\to+\infty$, anche $b_n\to+\infty$; analogo con maggiorante a $-\infty$. |
| [[84 Confronto in Modulo e Prodotto con un Infinitesimo\|Limitata × infinitesima]] | $\lvert a_n\rvert\leq M$ definitivamente e $b_n\to0\Rightarrow a_nb_n\to0$, anche se $a_n$ non ha limite. |
| [[78 Limiti di Potenze e Progressioni Geometriche\|Progressione geometrica]] | $q^n\to0$ per $\lvert q\rvert<1$; vale $1$ per $q=1$; tende a $+\infty$ per $q>1$; è irregolare per $q\leq-1$. |
| [[91 Criterio del Rapporto per Successioni\|Rapporto per successioni]] | $a_n>0$ definitivamente, $a_{n+1}/a_n\to L\in[0,+\infty]$: $L<1\Rightarrow a_n\to0$; $L>1\Rightarrow a_n\to+\infty$; $L=1$ non decide. |
| [[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate\|Forme indeterminate]] · [[89 Limiti di Potenze con Base ed Esponente Variabili\|potenze variabili]] | $0/0$, $\infty/\infty$, $0\cdot\infty$, $\infty-\infty$, $1^{\pm\infty}$, $0^0$, $\infty^0$ richiedono studio. Con $a_n>0$: $a_n^{b_n}=e^{b_n\log a_n}$. |

[[03 Formulario#Indice rapido|↑ Indice]]
