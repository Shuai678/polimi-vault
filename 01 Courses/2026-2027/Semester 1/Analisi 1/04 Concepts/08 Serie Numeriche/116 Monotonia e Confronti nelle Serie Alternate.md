---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 12, PDF pp. 19-24
---

# Monotonia e confronti nelle serie alternate

## Il punto delicato

Il [[115 Serie Alternate e Criterio di Leibniz|criterio di Leibniz]] richiede che l'ampiezza sia non crescente almeno definitivamente. Il fatto che tenda a zero non sostituisce questa ipotesi. Nemmeno essere equivalente a una successione decrescente garantisce di essere decrescente: l'equivalenza controlla l'errore relativo, non l'ordine fra termini consecutivi.

Il [[109 Criterio del Confronto Asintotico per Serie|confronto asintotico per serie]] studiato finora riguarda termini definitivamente positivi. Non lo si può estendere automaticamente a due serie a segni alterni, neppure se le rispettive ampiezze positive sono equivalenti.

## Controesempio del docente

### Costruzione

Per $n\geq1$, poniamo

$$
a_n=\frac{\sqrt n+(-1)^n}{n}
=\frac1{\sqrt n}+\frac{(-1)^n}{n},
\qquad b_n=\frac1{\sqrt n}.
$$

Abbiamo $a_1=0$ e $a_n>0$ per $n\geq2$, mentre $b_n>0$. Entrambe le successioni tendono a zero. Inoltre

$$
\frac{a_n}{b_n}
=1+\frac{(-1)^n}{\sqrt n}\longrightarrow1,
\qquad a_n\sim b_n.
$$

La successione $b_n$ è decrescente e $\sum(-1)^n b_n$ converge per Leibniz.

### La serie con ampiezza equivalente diverge

Per ogni somma finita,

$$
\sum_{n=1}^{N}(-1)^n a_n
=\sum_{n=1}^{N}\left(\frac{(-1)^n}{\sqrt n}+\frac1n\right)
=\sum_{n=1}^{N}\frac{(-1)^n}{\sqrt n}+\sum_{n=1}^{N}\frac1n.
$$

La prima somma parziale ha limite finito; la seconda tende a $+\infty$ per l'[[104 Serie Armonica|armonica]]. Di conseguenza

$$
\boxed{\sum_{n=1}^{+\infty}(-1)^n a_n=+\infty,\qquad
\sum_{n=1}^{+\infty}(-1)^n b_n\text{ converge}.}
$$

L'errore relativo fra le ampiezze tende a zero, ma dopo la moltiplicazione per $(-1)^n$ produce il contributo positivo $1/n$, la cui serie diverge. La manipolazione è giustificata prima sulle somme finite e poi attraverso i loro limiti.

### Perché $a_n$ non è definitivamente non crescente

La divergenza appena provata, insieme ad $a_n\geq0$ e $a_n\to0$, mostra già che l'ipotesi di monotonia di Leibniz deve fallire. Possiamo anche verificarlo direttamente.

Per $n$ dispari,

$$
a_{n+1}-a_n
=\frac1{\sqrt{n+1}}-\frac1{\sqrt n}+\frac1{n+1}+\frac1n
=-\frac1{\sqrt n\sqrt{n+1}(\sqrt n+\sqrt{n+1})}
 +\frac1{n+1}+\frac1n>0.
$$

Infatti il modulo dell'unico contributo negativo è al più $1/(2n^{3/2})<1/n$. Ci sono dunque aumenti per infiniti indici. Per $n$ pari, invece,

$$
a_{n+1}-a_n
=\frac1{\sqrt{n+1}}-\frac1{\sqrt n}-\frac1{n+1}-\frac1n<0.
$$

La successione alterna aumenti e diminuzioni, anche arbitrariamente avanti.

![[116 Monotonia delle Ampiezze nelle Serie Alternate.svg|900]]

A sinistra, $a_n\sim b_n$ ma l'ampiezza $a_n$ non è monotona. A destra, l'ampiezza del prossimo esempio è invece decrescente nella coda. L'equivalenza non sostituisce questa verifica.

## Esempio del docente — $\sum(-1)^n\log n/n$

### Testo e idea

Studiare

$$
\sum_{n=1}^{+\infty}(-1)^n\frac{\log n}{n}.
$$

L'ampiezza è $a_n=\log n/n\geq0$, con $a_1=0$. Per la [[85 Gerarchia degli Infiniti|gerarchia]], $a_n\to0$. Serve ancora controllare la monotonia nella coda.

### La verifica del docente mediante una funzione

Il PDF considera $f(x)=\log x/x$ e calcola

$$
f'(x)=\frac{1-\log x}{x^2}.
$$

Per $x\geq e$, $f'(x)\leq0$, quindi $f$ è non crescente; in particolare $a_n=f(n)$ è decrescente per $n\geq3$.

> [!note] Anticipazione presente nel PDF
> Qui il docente usa derivata e legame fra segno della derivata e monotonia prima della trattazione sistematica. Il calcolo è conservato come nell'esempio, senza introdurre un nuovo capitolo sulle derivate. La verifica seguente permette di chiudere l'esercizio con gli strumenti sulle successioni già disponibili.

### Verifica alternativa senza derivate

Per $n\geq1$, moltiplicando per i denominatori positivi,

$$
\frac{\log(n+1)}{n+1}\leq\frac{\log n}{n}
\iff n\log(n+1)\leq(n+1)\log n
\iff n\log\left(1+\frac1n\right)\leq\log n.
$$

Dal Concept [[104 Serie Armonica|104]] sappiamo che $\log(1+1/n)\leq1/n$, dunque il membro sinistro è al più $1$. Per $n\geq4$ abbiamo $\log n\geq1$, usando la stima $e\leq4$ già ottenuta in [[90 Numero di Nepero e Limiti di Tipo Esponenziale]]. Pertanto $a_{n+1}\leq a_n$ almeno da $n=4$ in poi. È sufficiente: Leibniz richiede monotonia **definitiva**.

### Convergenza assoluta e risultato

La serie dei moduli è $\sum\log n/n$. Per $n\geq4$, $\log n\geq1$, quindi

$$
\frac{\log n}{n}\geq\frac1n.
$$

La serie dei moduli diverge per confronto con l'armonica. La serie originaria converge per Leibniz, ma **solo semplicemente**.

Non si può scrivere $\log n/n\sim1/n$: il rapporto fra queste due successioni è $\log n\to+\infty$. Avere lo stesso limite zero non significa essere equivalenti.

## Metodo per gli esercizi

Per una serie $\sum(-1)^n a_n$, identificare l'ampiezza, verificare il suo limite zero e dimostrarne la monotonia nella coda. Per la monotonia si può studiare $a_{n+1}-a_n$, confrontare $a_{n+1}/a_n$ con $1$ quando $a_n>0$, oppure usare una funzione associata con un criterio già giustificato. La sola equivalenza con un'ampiezza monotona non basta.

Se la serie dei moduli diverge, ciò esclude soltanto la convergenza assoluta. Per concludere sulla serie con segni bisogna ancora usare un criterio applicabile o studiare le somme parziali.

### Da dire all'orale

> Nel criterio di Leibniz la monotonia definitiva è un'ipotesi autonoma. Due ampiezze positive equivalenti possono produrre serie alternate di carattere diverso. Per esempio, aggiungere alla successione uno su radice di enne la quantità meno uno alla enne su enne genera, dopo l'alternanza, una serie armonica positiva: la nuova serie diverge pur avendo ampiezza equivalente alla precedente.
