---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 12, PDF pp. 11-16
  - Libro, §4.4, pp. 125-126, definizione 4.26 e teorema 4.27
  - Regolamento AM1 2026-2027, PDF p. 2, dimostrazione D14
---

# Convergenza assoluta e semplice delle serie

## Perché introdurre la convergenza assoluta

Per una serie a segno variabile i termini positivi e negativi possono compensarsi. Studiare la serie dei valori assoluti elimina queste compensazioni e consente di usare i criteri per [[106 Serie a Termini Positivi|serie non negative]]. Se persino la somma delle grandezze dei termini resta finita, converge anche la serie originaria.

La convergenza definita attraverso le [[99 Serie Numeriche e Somme Parziali|somme parziali]] viene ora chiamata anche **convergenza semplice**. L'aggettivo “semplice” da solo non esclude quella assoluta.

## Definizioni formali e notazione

Sia $(a_n)$ una successione reale, con indice iniziale $n_0$.

- $\sum_{n=n_0}^{+\infty}a_n$ **converge semplicemente** se $S_N=\sum_{n=n_0}^{N}a_n$ ha limite finito $S\in\mathbb R$.
- La serie **converge assolutamente** se converge la serie dei moduli:

$$
\boxed{\sum_{n=n_0}^{+\infty}|a_n|<+\infty.}
$$

- Una serie convergente semplicemente ma non assolutamente si dice **convergente solo semplicemente**, o **condizionatamente convergente**.

La serie dei moduli ha termini non negativi: o converge o diverge a $+\infty$. Non può essere irregolare. “Non converge assolutamente” non significa quindi che la serie originaria non converga: significa che $\sum|a_n|=+\infty$.

### Da dire all'orale — Definizione

> Una serie converge assolutamente quando converge la serie dei valori assoluti dei suoi termini. La convergenza semplice è la convergenza a un numero reale della successione delle somme parziali. Se vale la seconda ma non la prima, la convergenza è solo semplice.

## Teorema — Assoluta implica semplice

Se $\sum_{n=n_0}^{+\infty}|a_n|$ converge, allora converge anche $\sum_{n=n_0}^{+\infty}a_n$. Inoltre

$$
\boxed{
\left|\sum_{n=n_0}^{+\infty}a_n\right|
\leq\sum_{n=n_0}^{+\infty}|a_n|.
}
$$

**Ipotesi:** termini reali e convergenza della serie dei moduli. **Tesi:** esistenza della somma reale della serie originaria, con la stima indicata.

> [!info] Riferimento d'esame — D14
> La dimostrazione «La convergenza assoluta implica la convergenza semplice di una serie» è la D14 nell'elenco del [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2. La prova seguente segue il docente, pp. 13-15 del PDF L12; il libro la presenta nel teorema 4.27. Materiale ancora **Da studiare**.

## Strategia della dimostrazione

Costruiamo una successione non negativa, $a_n+|a_n|$, dominata da $2|a_n|$. Il confronto prova la convergenza della sua serie. Solo dopo aver ottenuto due serie convergenti possiamo sottrarre le loro somme e recuperare la serie di $a_n$.

## Dimostrazione passo per passo

### 1. Un confronto fra termini non negativi

Da $-|a_n|\leq a_n\leq|a_n|$, sommando $|a_n|$, otteniamo

$$
0\leq a_n+|a_n|\leq2|a_n|.
$$

La serie $\sum2|a_n|$ converge per ipotesi e [[101 Linearità e Algebra delle Serie|linearità]]. Per il [[107 Criterio del Confronto per Serie]] converge dunque anche $\sum(a_n+|a_n|)$.

### 2. Recuperare le somme parziali originarie

Poniamo

$$
P_N=\sum_{n=n_0}^{N}(a_n+|a_n|),
\qquad Q_N=\sum_{n=n_0}^{N}|a_n|.
$$

Esistono $P,Q\in\mathbb R$ tali che $P_N\to P$, $Q_N\to Q$. Per ogni indice finito $N$,

$$
S_N=\sum_{n=n_0}^{N}a_n=P_N-Q_N.
$$

L'[[80 Algebra dei Limiti di Successioni|algebra dei limiti finiti]] dà $S_N\to P-Q\in\mathbb R$. La serie originaria converge semplicemente. Non abbiamo separato serie di carattere ancora ignoto: abbiamo prima lavorato con somme finite e provato i limiti necessari.

### 3. La stima del modulo della somma

Per la [[30 Disuguaglianza Triangolare|disuguaglianza triangolare]], applicata ripetutamente a una somma finita,

$$
|S_N|=\left|\sum_{n=n_0}^{N}a_n\right|
\leq\sum_{n=n_0}^{N}|a_n|=Q_N.
$$

Se $S_N\to S$, anche $|S_N|\to|S|$, perché

$$
\bigl||S_N|-|S|\bigr|\leq|S_N-S|\to0.
$$

Passando al limite nella disuguaglianza otteniamo $|S|\leq Q$, cioè la stima del teorema.

## Esempi del docente

### Esempio 1 — $\sum_{n=1}^{+\infty}\sin n/n^{3/2}$

L'ampiezza $|\sin n|$ è al più $1$, quindi

$$
0\leq\left|\frac{\sin n}{n^{3/2}}\right|
\leq\frac1{n^{3/2}}.
$$

La serie maggiore è un'[[108 Serie Armoniche Generalizzate e di Bertrand|armonica generalizzata]] con esponente $3/2>1$. La serie dei moduli converge per confronto; quella originaria converge assolutamente e quindi semplicemente. Non occorre conoscere il segno di $\sin n$ per ogni intero.

### Esempio 2 — $\sum_{n=1}^{+\infty}(-1)^n/n^{3/2}$

Qui il modulo è esattamente $1/n^{3/2}$. La serie converge assolutamente per lo stesso criterio. Leibniz sarebbe applicabile, ma la convergenza assoluta dà già una conclusione più forte.

## Il viceversa è falso

Per $0<\alpha\leq1$, la serie

$$
\sum_{n=1}^{+\infty}\frac{(-1)^n}{n^\alpha}
$$

converge per [[115 Serie Alternate e Criterio di Leibniz|Leibniz]], mentre la serie dei moduli $\sum1/n^\alpha$ diverge. Il caso $\alpha=1$ è l'armonica alternata. Le compensazioni rendono possibile una somma finita pur con serie dei moduli infinita.

Se tutti i termini sono non negativi, invece, $|a_n|=a_n$: convergenza semplice e assoluta coincidono. Anche se la non negatività vale solo definitivamente, il carattere coincide, perché un numero finito di termini non influenza la convergenza.

## Uso negli esercizi ed errori comuni

Per una serie a segno variabile, studiare $\sum|a_n|$ è spesso il primo tentativo utile. Se converge, il problema della convergenza è risolto. Se diverge, occorre tornare ai segni: la serie originaria può convergere solo semplicemente, divergere o essere irregolare.

La stima $|\sum a_n|\leq\sum|a_n|$ non è un'uguaglianza in generale. Non spostare il valore assoluto attraverso la somma come se i segni fossero tutti concordi. La sola proprietà $a_n\to0$ continua a essere necessaria e non sufficiente.

### Da dire all'orale — Teorema e prova

> La convergenza assoluta implica quella semplice. Per provarlo osservo che zero è minore o uguale ad a enne più il suo valore assoluto, e questa quantità è al più due volte il valore assoluto di a enne. Il confronto dà la convergenza della serie di queste quantità; sottraendo la serie convergente dei moduli ottengo quella originaria. La disuguaglianza triangolare sulle somme parziali e il passaggio al limite danno la stima sul modulo della somma.
