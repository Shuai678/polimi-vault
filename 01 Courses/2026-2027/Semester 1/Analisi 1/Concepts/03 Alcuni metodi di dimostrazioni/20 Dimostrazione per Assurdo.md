---
course: Analisi 1
type: method
status: studied
source:
  - Lezione 01, PDF pp. 18-19
  - Libro, cap. 1.1.5, p. 6
---

# Dimostrazione per assurdo

## Intuizione

Per dimostrare una tesi si assume temporaneamente che essa sia falsa. Se questa supposizione conduce a una contraddizione, la negazione della tesi non può essere vera e quindi la tesi è vera.

## Metodo

Per dimostrare una tesi $Q$ per assurdo:

1. si assume vera la negazione $\neg Q$;
2. si deducono conseguenze usando le ipotesi e risultati già noti;
3. si ottiene una contraddizione, cioè una proposizione $S$ insieme alla sua negazione $\neg S$;
4. si conclude che $\neg Q$ è falsa e quindi che $Q$ è vera.

Per dimostrare un'implicazione $P\Rightarrow Q$, si assumono contemporaneamente $P$ e $\neg Q$ e si cerca una contraddizione.

### Da dire all'orale

> In una dimostrazione per assurdo assumo vera la negazione della tesi e mostro che questa supposizione conduce a una contraddizione. Concludo quindi che la negazione della tesi è falsa e che la tesi è vera.

## Condizioni

- La negazione della tesi deve essere formulata correttamente.
- La contraddizione deve derivare dalla supposizione introdotta e dalle altre ipotesi.
- Bisogna indicare esplicitamente quali due affermazioni incompatibili sono state ottenute.

## Esempi

### Esempio introduttivo svolto: inesistenza del massimo naturale

Vogliamo dimostrare che non esiste un massimo numero naturale.

1. **Negazione della tesi.** Supponiamo per assurdo che esista un massimo $M\in\mathbb N$.
2. **Conseguenza della supposizione.** Poiché $M$ è naturale, anche $M+1$ è naturale.
3. **Confronto.** Per costruzione, $M+1>M$.
4. **Contraddizione.** $M$ dovrebbe essere il massimo naturale, ma abbiamo trovato il naturale $M+1$ che è maggiore di $M$.
5. **Conclusione.** La supposizione iniziale è falsa; quindi non esiste un massimo numero naturale.

### Esempio principale della lezione: irrazionalità di $\sqrt2$

Vogliamo dimostrare che

$$
\sqrt2\notin\mathbb Q.
$$

**1. Supposizione per assurdo.** Supponiamo che la tesi sia falsa, cioè che $\sqrt2\in\mathbb Q$.

**2. Rappresentazione come frazione ridotta.** Essendo razionale, $\sqrt2$ si può scrivere come

$$
\sqrt2=\frac mn,
$$

con $m,n\in\mathbb Z$, $n\ne0$ e $m,n$ primi tra loro. Scegliere la frazione ridotta è essenziale: significa che $m$ e $n$ non hanno divisori primi comuni.

**3. Eliminazione della radice e del denominatore.** Elevando al quadrato otteniamo

$$
2=\frac{m^2}{n^2}.
$$

Moltiplicando entrambi i membri per $n^2$, operazione lecita perché $n\ne0$, segue

$$
m^2=2n^2.
$$

**4. Parità di $m$.** L'uguaglianza mostra che $m^2$ è pari. Dal risultato “se il quadrato di un intero è pari, allora l'intero è pari” segue che $m$ è pari. Esiste quindi $k\in\mathbb Z$ tale che

$$
m=2k.
$$

**5. Parità di $n$.** Sostituiamo $m=2k$ nell'uguaglianza $m^2=2n^2$:

$$
(2k)^2=2n^2.
$$

Sviluppando e dividendo entrambi i membri per $2$:

$$
4k^2=2n^2
\quad\Longrightarrow\quad
n^2=2k^2.
$$

Quindi anche $n^2$ è pari e, per lo stesso risultato precedente, $n$ è pari.

**6. Contraddizione.** Sia $m$ sia $n$ sono pari, quindi sono entrambi divisibili per $2$. Ma erano stati scelti primi tra loro. Le due affermazioni sono incompatibili.

**7. Conclusione.** La supposizione $\sqrt2\in\mathbb Q$ è falsa. Pertanto

$$
\sqrt2\notin\mathbb Q.
$$

Questa dimostrazione è presente nella lezione e nel libro, ma deve ancora essere verificata in una sessione interattiva.

## Errori comuni

- Assumere la tesi invece della sua negazione.
- Ottenere una contraddizione senza precisare quali affermazioni siano incompatibili.
- Concludere che il teorema è falso: è falsa la supposizione introdotta per assurdo.

## Connessioni

- Nella dimostrazione dell'irrazionalità di $\sqrt{2}$ si suppone che $\sqrt{2}$ sia razionale e si conclude che numeratore e denominatore di una frazione ridotta sono entrambi pari.
- La dimostrazione per assurdo usa la negazione logica e il principio di non contraddizione.

## Prospettiva d'esame

All'orale conviene dichiarare subito la supposizione per assurdo, indicare il punto preciso in cui nasce la contraddizione e spiegare perché essa rende falsa la supposizione iniziale.
