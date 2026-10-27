---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 18-19
  - Libro, §3.7, p. 100 (limite del termine); §4.2.2, pp. 121-123 (criteri sulle serie)
---

# Formula di Stirling e serie con fattoriali

## Perché serve

La [[85 Gerarchia degli Infiniti|gerarchia]] dice che $n!$ è trascurabile rispetto a $n^n$, ma non descrive la scala precisa del rapporto. La formula di Stirling fornisce un equivalente del fattoriale e permette di trasformare termini che lo contengono in prodotti di potenze e fattori esponenziali.

## Enunciato della formula

Per $n\to+\infty$,

$$
\boxed{n!\sim\sqrt{2\pi n}\left(\frac ne\right)^n.}
$$

Il significato formale è

$$
\frac{n!}{\sqrt{2\pi n}(n/e)^n}\to1.
$$

È un'equivalenza asintotica, non un'uguaglianza esatta. L'errore **relativo** tende a zero; non si afferma che la differenza assoluta fra i due membri tenda a zero. La formula è enunciata e usata nel PDF senza dimostrazione.

![[112 Accuratezza Relativa della Formula di Stirling.svg|900]]

Il grafico mostra il rapporto che tende a $1$; i valori numerici illustrano l'enunciato e non ne costituiscono una dimostrazione.

### Da dire all'orale

> La formula di Stirling afferma che il fattoriale di n è asintoticamente equivalente alla radice quadrata di due pi greco n moltiplicata per n su e elevato a n. Il rapporto fra le due quantità tende a uno. Posso usarla per trovare equivalenti di termini con fattoriali, verificando poi le condizioni del criterio sulle serie.

## Esercizio — Due metodi per la stessa serie

### Testo

Studiare

$$
\sum_{n=1}^{+\infty}\frac{n!}{n^n}.
$$

I termini $a_n=n!/n^n$ sono positivi. Dal [[91 Criterio del Rapporto per Successioni|criterio del rapporto per successioni]] si ricava che $a_n\to0$, ma questa condizione da sola non decide la convergenza della serie.

### Metodo 1 — Criterio del rapporto

Usando $(n+1)!=(n+1)n!$,

$$
\begin{aligned}
\frac{a_{n+1}}{a_n}
&=\frac{(n+1)!}{(n+1)^{n+1}}\frac{n^n}{n!}\\
&=\frac{(n+1)n^n}{(n+1)^{n+1}}
=\left(\frac n{n+1}\right)^n.
\end{aligned}
$$

Nella forma del PDF,

$$
\left(\frac n{n+1}\right)^n
=\left(1-\frac1{n+1}\right)^{n+1}
\left(1-\frac1{n+1}\right)^{-1}
\to e^{-1}\cdot1=\frac1e<1.
$$

Il limite esponenziale è quello di [[90 Numero di Nepero e Limiti di Tipo Esponenziale]]. Equivalentemente, il rapporto è il reciproco di $(1+1/n)^n$. Per [[110 Criterio del Rapporto per Serie]],

$$
\boxed{\sum_{n=1}^{+\infty}\frac{n!}{n^n}\text{ converge}.}
$$

### Metodo 2 — Stirling e confronto asintotico

Dalla formula di Stirling, dividendo per la quantità positiva $n^n$,

$$
\begin{aligned}
a_n=\frac{n!}{n^n}
&\sim\frac{\sqrt{2\pi n}(n/e)^n}{n^n}\\
&=\frac{\sqrt{2\pi n}}{e^n}=:b_n.
\end{aligned}
$$

La semplificazione usa $(n/e)^n=n^n/e^n$: il fattore $\sqrt{2\pi n}$ deve essere mantenuto.

Per dimostrare che $\sum b_n$ converge, costruiamo il maggiorante scelto dal docente. Dalla gerarchia polinomio-esponenziale,

$$
\frac{\sqrt{2\pi n}}{2^n}\to0.
$$

Perciò definitivamente tale rapporto è minore o uguale a $1$ e

$$
0\leq b_n
=\frac{\sqrt{2\pi n}}{2^n}\left(\frac2e\right)^n
\leq\left(\frac2e\right)^n.
$$

Poiché $e>2$, già provato nel Concept 90, $0<2/e<1$. La geometrica maggiorante converge; il [[107 Criterio del Confronto per Serie]] dà la convergenza di $\sum b_n$. Infine $a_n\sim b_n$ e la positività consentono di applicare il [[109 Criterio del Confronto Asintotico per Serie]] e ritrovare la convergenza della serie originale.

### Cosa imparare

Il primo metodo è più breve; il secondo chiarisce la scala del termine e collega fattoriale, gerarchia ed equivalenza. Entrambi concludono sulla serie tramite un criterio. Il solo limite $n!/n^n\to0$ non sarebbe una dimostrazione di convergenza.

## Errori comuni e prospettiva d'esame

- Dimenticare la radice $\sqrt{2\pi n}$ o sostituirla con $\sqrt{2\pi}\,n$.
- Leggere $(n/e)^n$ come $n/e^n$.
- Usare la formula come identità esatta per ogni $n$.
- Trovare un equivalente senza studiare il carattere della sua serie.
- Confondere la gerarchia dei singoli termini con la convergenza della somma infinita.

Potenziale rilevanza d'esame: formulazione corretta di Stirling, rapporto con fattoriali e costruzione del confronto geometrico del PDF. La dimostrazione della formula di Stirling non è presente in questa lezione.
