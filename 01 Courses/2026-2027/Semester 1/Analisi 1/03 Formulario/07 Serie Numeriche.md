---
course: Analisi 1
type: formula-sheet
updated: 2026-10-29
cssclasses:
  - formulario
---

# Serie numeriche

[[00 Indice Formulario|Indice del formulario]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map/00 Course Map|Corso]]

**In questa scheda:** [[#Come studiare una serie — Schema operativo|Schema operativo]] · [[#Formule e teoremi essenziali|Formule e teoremi]] · [[#Convergenza assoluta e serie alternate|Serie alternate]]

> [!note] Integrazioni della Lezione 12 — Da studiare
> Convergenza assoluta e D14, Leibniz, cautele sulle alternate ed esponente variabile sono preparati per lo studio successivo.

## Come studiare una serie — Schema operativo

Consideriamo $\sum a_n$. Quando studiamo i moduli, scriviamo $b_n=\lvert a_n\rvert$: $b_n$ è l'**ampiezza**, distinta dal termine $a_n$ con il suo segno.

1. **Controllare il termine generale**

   Verificare se $a_n\to0$. Se non tende a zero, la serie **non converge**. Se tende a zero, bisogna proseguire: è una condizione necessaria, non sufficiente.

2. **Riconoscere i segni**

   Una serie a **segno misto senza alternanza regolare** presenta termini positivi e negativi, ma non necessariamente casuali. Una serie **alternata** ha la forma $\sum(-1)^n b_n$ oppure $\sum(-1)^{n+1}b_n$, con $b_n\geq0$ definitivamente: la non negatività riguarda l'ampiezza, non i termini con segno.

3. **Se i termini hanno segno costante definitivamente**

   Se $a_n\geq0$ definitivamente, usare un criterio per termini non negativi, scelto dallo schema seguente. Se $a_n\leq0$ definitivamente, studiare $\sum(-a_n)$ e poi ripristinare il segno.

4. **Se i termini cambiano segno, studiare i moduli**

   Studiare $\sum\lvert a_n\rvert$. Se converge, la serie originaria **converge assolutamente**, quindi converge anche con i segni.

5. **Se la serie dei moduli diverge**

   Si esclude soltanto la convergenza assoluta: la serie originaria **potrebbe ancora convergere**. Se non è alternata, servono altri strumenti applicabili o lo studio delle somme parziali.

6. **Se la serie è alternata, provare Leibniz**

   Verificare sull'ampiezza $b_n$ le tre condizioni: **$b_n\geq0$ definitivamente**, **$b_n\to0$**, **$b_{n+1}\leq b_n$ definitivamente**. Se valgono, la serie converge; se la serie dei moduli è stata provata divergente, converge **solo semplicemente**.

Studiare prima la convergenza assoluta è una strategia pratica, **non un requisito per applicare Leibniz**.

### Scelta del criterio per termini non negativi

Lo schema riguarda $\sum b_n$, con $b_n\geq0$ definitivamente. L'ordine è un promemoria, **non una regola obbligatoria**: radice, rapporto e confronto asintotico non sono sempre intercambiabili; scegliere quello che semplifica i calcoli.

- **[[111 Criterio della Radice per Serie|Radice]]** — Spesso utile con espressioni elevate a $n$. Calcolare $L=\lim\sqrt[n]{b_n}$: se $L<1$, converge; se $L>1$, diverge a $+\infty$; se $L=1$, **non conclude**.

- **[[110 Criterio del Rapporto per Serie|Rapporto]]** — Spesso utile con fattoriali e prodotti. Con $b_n>0$ definitivamente, calcolare $L=\lim b_{n+1}/b_n$: se $L<1$, converge; se $L>1$, diverge a $+\infty$; se $L=1$, **non conclude**.

- **[[109 Criterio del Confronto Asintotico per Serie|Confronto asintotico]]** — Spesso utile con potenze di $n$ e logaritmi. Trovare $c_n>0$ definitivamente con $b_n\sim c_n$, per $b_n>0$ definitivamente: le due serie hanno lo **stesso carattere**.

- **[[107 Criterio del Confronto per Serie|Confronto]]** — Se $0\leq b_n\leq c_n$ definitivamente e $\sum c_n$ converge, converge anche $\sum b_n$. Se $b_n\geq c_n\geq0$ definitivamente e $\sum c_n$ diverge, diverge anche $\sum b_n$.

### Cautele e promemoria

> [!warning] Asintotici e serie alternate
> **Asintotici e Leibniz** — Un equivalente può aiutare a provare che $b_n\to0$, ma **non garantisce la monotonia**. Non basta sostituire $b_n$ con un equivalente decrescente per applicare Leibniz.
>
> **Asintotici e serie alternate** — Il confronto asintotico per serie studiato qui riguarda termini definitivamente positivi. **Due ampiezze positive equivalenti non garantiscono lo stesso carattere delle rispettive serie alternate**: vedi [[116 Monotonia e Confronti nelle Serie Alternate|monotonia ed equivalenze]].
>
> **Asintotici e convergenza assoluta** — Si possono usare sulla **serie dei moduli**: se $\lvert a_n\rvert\sim c_n$ con $c_n>0$ definitivamente, $\sum\lvert a_n\rvert$ e $\sum c_n$ hanno lo stesso carattere.
>
> **Verificare la monotonia** — Dimostrare $b_{n+1}-b_n\leq0$ definitivamente oppure, se $b_n>0$, $b_{n+1}/b_n\leq1$ definitivamente. Basta essere **non crescente**, non necessariamente strettamente decrescente.

> [!note]- Altri promemoria
> **Un criterio può non concludere** — Per radice e rapporto, $L=1$ non decide; se il limite non esiste, la versione del criterio qui riportata non si applica. La mancata monotonia richiesta da Leibniz non prova la mancata convergenza: occorre un altro argomento.
>
> **I primi termini non decidono il carattere** — Aggiungere, eliminare o modificare un numero **finito** di termini non cambia il carattere della serie, ma può cambiarne la somma. Per questo molte ipotesi bastano **definitivamente**.
>
> **Serie di riferimento** — La [[100 Serie Geometrica e Rappresentazioni Decimali|geometrica]] $\sum q^n$ converge se e solo se $\lvert q\rvert<1$. L'[[108 Serie Armoniche Generalizzate e di Bertrand|armonica generalizzata]] $\sum 1/n^p$ converge se e solo se $p>1$.
>
> **Errore con Leibniz** — Se valgono le ipotesi di Leibniz, indicando con $S$ la somma e con $S_N$ la somma fino all'indice $N$, vale $\lvert S-S_N\rvert\leq b_{N+1}$ per $N$ nella coda in cui valgono le ipotesi: l'errore è al più l'ampiezza del primo termine trascurato.
>
> **Non convergenza e somme parziali** — Non convergere non significa necessariamente tendere a infinito. Se le somme parziali tendono a $+\infty$ o $-\infty$, la serie è **divergente**; se non hanno limite nemmeno nei reali estesi, è **irregolare**.

## Formule e teoremi essenziali

### Definizione e algebra

#### Serie e somme parziali

[[99 Serie Numeriche e Somme Parziali|Serie e somme parziali]]

$$
S_N=\sum_{n=n_0}^{N}a_n.
$$

| Somme parziali | Carattere della serie |
| --- | --- |
| $S_N\to S\in\mathbb R$ | Convergente. |
| $S_N\to\pm\infty$ | Divergente. |
| Nessun limite nei reali estesi | Irregolare. |

#### Condizione necessaria · D10

[[103 Condizione Necessaria di Convergenza di una Serie|Condizione necessaria]] · [[D10 Condizione Necessaria di Convergenza di una Serie|Dimostrazione D10]]

$$
\sum a_n\text{ convergente}\Rightarrow a_n\to0.
$$

**Nella prova:** $a_N=S_N-S_{N-1}$.

**Il viceversa è falso:** la serie armonica diverge.

#### Linearità e resto

[[101 Linearità e Algebra delle Serie|Linearità]] · [[105 Code e Resto di una Serie|resto]]

**Per serie convergenti:**

$$
\sum(\alpha a_n+\beta b_n)=\alpha\sum a_n+\beta\sum b_n.
$$

**Resto della serie**

$$
R_N=\sum_{n=N+1}^{\infty}a_n=S-S_N\to0.
$$

Cambiare finiti termini conserva il **carattere**, ma non necessariamente la **somma**.

#### Termini non negativi

[[106 Serie a Termini Positivi|Termini non negativi]]

**Ipotesi:** $a_n\geq0$ definitivamente.

La serie **converge o diverge a $+\infty$**. Converge se e solo se le somme parziali sono **limitate superiormente**.

### Serie di riferimento

#### Serie geometrica

[[100 Serie Geometrica e Rappresentazioni Decimali|Serie geometrica]]

Per $q\neq1$:

$$
\sum_{n=0}^{N}q^n=\frac{1-q^{N+1}}{1-q}.
$$

La serie converge **se e solo se $\lvert q\rvert<1$**. In tal caso:

$$
\sum_{n=0}^{\infty}q^n=\frac1{1-q},
\qquad\sum_{n=1}^{\infty}q^n=\frac q{1-q}.
$$

#### Telescopiche e Mengoli

[[102 Serie Telescopiche e Serie di Mengoli|Telescopiche e Mengoli]]

**Ipotesi:** $a_n=b_n-b_{n+1}$.

$$
\sum_{n=m}^{N}a_n=b_m-b_{N+1}.
$$

Se $b_n\to b\in\mathbb R$, la somma è $b_m-b$.

**Serie di Mengoli**

$$
\sum_{n=1}^{\infty}\frac1{n(n+1)}=1.
$$

#### Armonica e armoniche generalizzate

[[104 Serie Armonica|Armonica]] · [[108 Serie Armoniche Generalizzate e di Bertrand|armoniche generalizzate]]

$$
\sum_{n=1}^{\infty}\frac1n=+\infty.
$$

$$
\sum_{n=1}^{\infty}\frac1{n^\alpha}\text{ converge}\iff\alpha>1.
$$

#### Serie di Bertrand

[[108 Serie Armoniche Generalizzate e di Bertrand|Serie di Bertrand]]

$$
\sum_{n=2}^{\infty}\frac1{n^\alpha(\log n)^\beta}.
$$

**Converge** se $\alpha>1$, oppure se $\alpha=1$ e $\beta>1$.

**Diverge** negli altri casi.

#### Stirling

[[112 Formula di Stirling e Serie con Fattoriali|Stirling]]

$$
n!\sim\sqrt{2\pi n}\left(\frac ne\right)^n.
$$

Quindi:

$$
\frac{n!}{n^n}\sim\frac{\sqrt{2\pi n}}{e^n}.
$$

### Criteri per termini non negativi

#### Confronto · D11

[[107 Criterio del Confronto per Serie|Confronto]] · [[D11 Teorema del Confronto per le Serie|Dimostrazione D11]]

**Ipotesi:** $0\leq a_n\leq b_n$ definitivamente.

$$
\begin{aligned}
\sum b_n\text{ convergente}&\Rightarrow\sum a_n\text{ convergente},\\
\sum a_n=+\infty&\Rightarrow\sum b_n=+\infty.
\end{aligned}
$$

#### Confronto asintotico · D12

[[109 Criterio del Confronto Asintotico per Serie|Confronto asintotico]] · [[D12 Teorema del Confronto Asintotico per le Serie|Dimostrazione D12]]

**Ipotesi:** $a_n,b_n>0$ definitivamente.

$$
\frac{a_n}{b_n}\to1\Rightarrow\text{stesso carattere delle due serie}.
$$

#### Rapporto per serie · D13

[[110 Criterio del Rapporto per Serie|Rapporto per serie]] · [[D13 Criterio del Rapporto per le Serie Numeriche|Dimostrazione D13]]

**Ipotesi:** $a_n>0$ definitivamente ed esiste

$$
L=\lim\frac{a_{n+1}}{a_n}\in[0,+\infty].
$$

| Valore di $L$ | Conclusione |
| --- | --- |
| $L<1$ | Converge. |
| $L>1$ | Diverge a $+\infty$. |
| $L=1$ | **Non decide.** |

#### Radice per serie

[[111 Criterio della Radice per Serie|Radice per serie]]

**Ipotesi:** $a_n\geq0$ definitivamente ed esiste

$$
L=\lim\sqrt[n]{a_n}\in[0,+\infty].
$$

| Valore di $L$ | Conclusione |
| --- | --- |
| $L<1$ | Converge. |
| $L>1$ | Diverge a $+\infty$. |
| $L=1$ | **Non decide.** |

### Convergenza assoluta e serie alternate

#### Convergenza assoluta ⇒ semplice · D14

[[114 Convergenza Assoluta e Semplice delle Serie|Convergenza assoluta ⇒ semplice]] · [[D14 Convergenza Assoluta Implica Convergenza Semplice|Dimostrazione D14]]

$$
\sum\lvert a_n\rvert<+\infty\Rightarrow\sum a_n\in\mathbb R.
$$

$$
\left\lvert\sum a_n\right\rvert\leq\sum\lvert a_n\rvert.
$$

**Idea della prova:** usare $0\leq a_n+\lvert a_n\rvert\leq2\lvert a_n\rvert$, il confronto e la differenza di due serie convergenti.

**Il viceversa è falso.**

#### Leibniz e resto

[[115 Serie Alternate e Criterio di Leibniz|Leibniz e resto]]

Per $\sum(-1)^n a_n$, verificare sull'ampiezza:

1. $a_n\geq0$ definitivamente.
2. $a_{n+1}\leq a_n$ definitivamente.
3. $a_n\to0$.

**Conclusione:** la serie converge e, per $N$ nella coda valida,

$$
\lvert S-S_N\rvert\leq a_{N+1}.
$$

Se le ipotesi valgono globalmente, la stima vale per ogni indice.

#### Convergenza solo semplice e armonica alternata

[[114 Convergenza Assoluta e Semplice delle Serie|Solo semplice]] · [[115 Serie Alternate e Criterio di Leibniz|armonica alternata]]

**Solo semplice:** la serie converge e la serie dei moduli diverge.

Per $\sum(-1)^n/n^\alpha$:

| Esponente | Carattere |
| --- | --- |
| $\alpha>1$ | Convergenza assoluta. |
| $0<\alpha\leq1$ | Convergenza solo semplice. |
| $\alpha\leq0$ | Irregolare. |

#### Monotonia ed equivalenze

[[116 Monotonia e Confronti nelle Serie Alternate|Monotonia ed equivalenze]]

> [!warning] Equivalenza e monotonia
> Ampiezze positive equivalenti non garantiscono uguale carattere delle rispettive serie alternate, né la monotonia dell'ampiezza. La monotonia definitiva richiesta da Leibniz va verificata.

### Esponente variabile

#### Potenza con esponente variabile

[[118 Equivalenti con Esponente Variabile nelle Serie|Potenza con esponente variabile]]

**Ipotesi:** $\varepsilon_n\to0$, $c_n\varepsilon_n\to0$, base positiva e fattori non nulli definitivamente.

$$
(1+\varepsilon_n)^{c_n}-1\sim c_n\varepsilon_n.
$$

**Passaggio da controllare:** scrivere

$$
e^{c_n\log(1+\varepsilon_n)}-1
$$

e verificare che l'esponente tenda a zero.

---

[[06 Equivalenti e Limiti Notevoli|← Equivalenti e Limiti Notevoli]] · [[00 Indice Formulario#Indice rapido|↑ Indice]] · [[08 Formulario Unico dei Limiti|Formulario Unico dei Limiti →]]
