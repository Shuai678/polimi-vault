---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 13, PDF pp. 7-9
---

# Definizione topologica di limite e teorema ponte

## Definizione topologica del docente

Siano $f:I\subseteq\mathbb R\to\mathbb R$, $x_0\in\overline{\mathbb R}$ punto di accumulazione per $I$ e $\ell\in\overline{\mathbb R}$. Si ha

$$
\lim_{x\to x_0}f(x)=\ell
$$

se e solo se, per **ogni** intorno $\mathcal U(\ell)$ di $\ell$, **esiste** un intorno $\mathcal U(x_0)$ di $x_0$ tale che

$$
\boxed{
x\in(\mathcal U(x_0)\cap I)\setminus\{x_0\}
\Longrightarrow f(x)\in\mathcal U(\ell).
}
$$

La richiesta sui valori di $f$ determina quanto restringere la zona del dominio. L'intorno di $x_0$ può dipendere dall'intorno scelto per $\ell$.

## Teorema ponte

La [[121 Limite di Funzione e Definizione Successionale|definizione successionale]] e la definizione topologica sono equivalenti, con le ipotesi appena indicate.

> [!note] Dimostrazione nel materiale del docente
> Nel PDF, p. 8, il teorema ponte è indicato **«no dim.»**. Qui se ne riportano enunciato e impiego, senza attribuire al professore una prova aggiuntiva.

## Osservazione del docente: recuperare le successioni

Ponendo $I=\mathbb N$ e $x_0=+\infty$, la funzione $f(n)$ è una successione. La definizione tramite intorni restituisce le definizioni già studiate:

- per $\ell=+\infty$: per ogni $M\in\mathbb R$ esiste $N$ tale che $n>N$ implica $f(n)>M$;
- per $\ell=-\infty$: per ogni $M\in\mathbb R$ esiste $N$ tale che $n>N$ implica $f(n)<M$;
- per $\ell\in\mathbb R$: per ogni $\varepsilon>0$ esiste $N$ tale che

$$
n>N\Longrightarrow\ell-\varepsilon<f(n)<\ell+\varepsilon,
\quad\text{ossia }|f(n)-\ell|<\varepsilon.
$$

## Esistenza e negazione del limite — ordine del PDF

**Esiste un limite nella retta estesa** se e solo se

$$
\exists\ell\in\overline{\mathbb R}\ \forall\mathcal U(\ell)
\exists\mathcal U(x_0)\ \forall x\in(\mathcal U(x_0)\cap I)\setminus\{x_0\}:
\quad f(x)\in\mathcal U(\ell).
$$

**Non esiste alcun limite nella retta estesa** se e solo se

$$
\forall\ell\in\overline{\mathbb R}\ \exists\mathcal U(\ell)
\forall\mathcal U(x_0)\ \exists x\in(\mathcal U(x_0)\cap I)\setminus\{x_0\}:
\quad f(x)\notin\mathcal U(\ell).
$$

## Commenti ai quantificatori

La negazione di “il limite è questo particolare $\ell$” non è ancora la negazione dell'esistenza di **ogni** limite. Nell'ultima formula dobbiamo respingere tutti i candidati $\ell$, compresi gli infiniti. Si usano le regole di [[14 Negazione Logica]].

L'ordine “per ogni intorno di arrivo, esiste un intorno di partenza” è essenziale. Invertirlo consentirebbe di scegliere la precisione dopo aver visto i punti, cambiando la definizione.

Nei [[124 Limiti Finiti all'Infinito e Asintoti Orizzontali|casi metrici]] espliciteremo gli intorni con soglie, $\varepsilon$ e $\delta$. Non occorre che $f$ sia definita in $x_0$; occorre sempre restringere $x$ ai punti del dominio.

### Da dire all'orale

> Il limite è elle quando, fissato qualunque intorno di elle, esiste un intorno del punto di partenza tale che tutti i punti del dominio in quell'intorno, escluso il centro, hanno immagine nell'intorno fissato di elle. Il teorema ponte rende equivalente questa formulazione a quella successionale.
