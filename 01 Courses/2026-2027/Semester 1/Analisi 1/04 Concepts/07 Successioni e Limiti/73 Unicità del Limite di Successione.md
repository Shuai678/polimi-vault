---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 06, PDF pp. 13-14
  - Libro, §3.2, pp. 80-81
---

# Unicità del limite di successione

## Teorema

Se una successione $(a_n)$ ammette limite finito, tale limite è unico.

## Dimostrazione per assurdo

Supponiamo che la stessa successione abbia due limiti distinti $\ell_1$ e $\ell_2$. Senza perdita di generalità, sia

$$
\ell_1>\ell_2.
$$

Scegliamo

$$
\varepsilon=\frac{\ell_1-\ell_2}{3}>0.
$$

Dalla convergenza a $\ell_1$ esiste $N_1$ tale che, per ogni $n\geq N_1$,

$$
a_n\in(\ell_1-\varepsilon,\ell_1+\varepsilon).
$$

Dalla convergenza a $\ell_2$ esiste $N_2$ tale che, per ogni $n\geq N_2$,

$$
a_n\in(\ell_2-\varepsilon,\ell_2+\varepsilon).
$$

Ponendo $N=\max\{N_1,N_2\}$, per ogni $n\geq N$ il termine $a_n$ dovrebbe appartenere contemporaneamente a entrambi gli intervalli.

![[73 Unicita Limite Successione.svg|624]]

Ma gli intervalli sono disgiunti. Infatti

$$
\ell_2+\varepsilon<\ell_1-\varepsilon
$$

perché $2\varepsilon=2(\ell_1-\ell_2)/3<\ell_1-\ell_2$. Si ottiene una contraddizione. Dunque $\ell_1=\ell_2$.

## Perché compare il massimo

$N_1$ garantisce la prima condizione e $N_2$ la seconda. Soltanto scegliendo

$$
N=\max\{N_1,N_2\}
$$

si è certi che entrambe valgano per gli stessi indici.

### Da dire all'orale

> Se esistessero due limiti distinti, potrei scegliere due intorni abbastanza piccoli da renderli disgiunti. I termini sufficientemente avanzati dovrebbero stare in entrambi, il che è impossibile.

## Errori comuni

- Dire soltanto che i due limiti sono diversi senza costruire intorni disgiunti.
- Usare $N_1$ o $N_2$ separatamente invece del loro massimo.
- Scegliere $\varepsilon$ senza controllare che gli intervalli siano disgiunti.
- Usare l'unicità del limite come ipotesi implicita nella sua stessa dimostrazione.

## Connessioni

- Parte dalla definizione di [[72 Limite Finito di una Successione|limite finito]].
- Usa la tecnica di [[20 Dimostrazione per Assurdo|dimostrazione per assurdo]].
- L'unicità si estende ai limiti nella retta reale estesa in [[74 Limiti Infiniti e Regolarità delle Successioni|limiti infiniti e regolarità]].

## Prospettiva d'esame

La dimostrazione va saputa ricostruire: ipotesi di due limiti, scelta di $\varepsilon$, due soglie, loro massimo e contraddizione dovuta agli intorni disgiunti.
