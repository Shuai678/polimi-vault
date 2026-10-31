---
course: Analisi 1
type: formula-sheet
updated: 2026-10-30
cssclasses:
  - formulario
---

# Guida agli esercizi su successioni e limiti

[[00 Indice Formulario|Indice del formulario]] · [[05 Successioni e Limiti|Teoria delle successioni]] · [[Potenze di n nei Limiti|Potenze di n]]

$$
\boxed{\text{FORMA}\longrightarrow\text{METODO}\longrightarrow\text{RISULTATO}}
$$

**In questa scheda:** [[#Tabella delle 7 forme indeterminate|Forme indeterminate]] · [[#Scegliere la tecnica di calcolo|Scelta del metodo]] · [[#Forme non indeterminate|Casi diretti]] · [[#Procedura per impostare un esercizio|Procedura]]

**Ipotesi:** $n\to+\infty$, costanti fissate, $\log=\ln$, angoli in radianti. Controllare domini e segni; per le potenze reali variabili si assumono basi positive definitivamente.

## Tabella delle 7 forme indeterminate

| Forma | Metodo da provare | Esempio → risultato |
| --- | --- | --- |
| $\dfrac00$ | Equivalenti, semplificazione, razionalizzazione | $\dfrac{\sin(1/n)}{1/n}\to1$ |
| $\dfrac\infty\infty$ | Gerarchia, termine dominante | $\dfrac{n^2}{e^n}\to0$ |
| $\infty-\infty$ | Razionalizzazione, raccoglimento | $\sqrt{n^2+n}-n\to\dfrac12$ |
| $0\cdot\infty$ | Trasformare in quoziente | $ne^{-n}=\dfrac{n}{e^n}\to0$ |
| $1^\infty$ | Limite notevole, logaritmo | $\left(1+\dfrac2n\right)^n\to e^2$ |
| $0^0$ | Logaritmo: studiare $b_n\log a_n$ | $\left(\dfrac1n\right)^{1/n}\to1$ |
| $\infty^0$ | Termine dominante, logaritmo | $(1+5^n)^{1/n}\to5$ |

> [!warning] Forma e risultato
> Il risultato dipende dall'espressione: quelli in tabella valgono per gli esempi. Anche $1^{-\infty}$ è indeterminata. Le sette forme non sono sette ricette universali.

## Scegliere la tecnica di calcolo

| Espressione riconosciuta | Metodo |
| --- | --- |
| Rapporto di polinomi | Raccogliere il termine di grado massimo in numeratore e denominatore. |
| Logaritmi, potenze di $n$, esponenziali, fattoriali | [[06 Equivalenti e Limiti Notevoli#Gerarchia degli infiniti\|Gerarchia degli infiniti]]. |
| Somma di esponenziali con basi positive sotto radice $n$-esima | Raccogliere l'esponenziale dominante. |
| Radice $n$-esima di un polinomio positivo definitivamente | Limite noto oppure logaritmo. |
| $\left(1+\dfrac an\right)^n$, $a$ fissato | Limite notevole: $e^a$. |
| $\sin t$, $1-\cos t$, $\log(1+t)$, $e^t-1$, con $t\to0$ | [[06 Equivalenti e Limiti Notevoli#Equivalenti per argomento infinitesimo\|Equivalenti notevoli]]. |
| Differenza di radici quadrate | Razionalizzare con il coniugato. |
| Potenza $a_n^{b_n}$, con $a_n>0$ | Scrivere $a_n^{b_n}=e^{b_n\log a_n}$. |
| Termini oscillanti | Confronto se smorzati; sottosuccessioni per mostrare che il limite non esiste. |
| Prodotti o fattoriali che si semplificano tra indici consecutivi | [[91 Criterio del Rapporto per Successioni\|Criterio del rapporto]], per successioni positive. |

**Cancellazioni:** nelle somme e differenze gli equivalenti principali possono non bastare; conservare i resti alla precisione necessaria.

## Forme non indeterminate

Le forme descrivono il comportamento al limite. Rispettare segni e dominio; $c$ è finito.

| Forma | Risultato |
| --- | --- |
| $\dfrac{c}{+\infty}$, $c\in\mathbb R$ | $0$ |
| $\dfrac{+\infty}{c}$, $c>0$ | $+\infty$ |
| $+\infty+(+\infty)$ | $+\infty$ |
| $0\cdot0$ | $0$ |
| $+\infty\cdot(+\infty)$ | $+\infty$ |
| $c^0$, $c>0$ | $1$ |
| $0^c$, $c>0$ | $0$ |
| $c^{+\infty}$, $c>1$ | $+\infty$ |
| $c^{+\infty}$, $0<c<1$ | $0$ |

## Procedura per impostare un esercizio

1. **Dominio e forma:** studiare i singoli termini e riconoscere l'eventuale indeterminazione.
2. **Metodo:** scegliere dalla tabella in base alle funzioni presenti; se ci sono oscillazioni, valutare confronto o sottosuccessioni.
3. **Calcolo:** trasformare l'espressione e verificare le ipotesi; ripetere se compare un'altra indeterminazione.
4. **Risultato:** applicare il limite noto o il teorema opportuno e giustificare il passaggio decisivo.

**Altri strumenti:** definizioni, confronti, monotonia e criterio del rapporto in [[05 Successioni e Limiti]]; valori da ricordare in [[08 Formulario Unico dei Limiti]].

---

[[00 Indice Formulario#Indice rapido|↑ Indice]] · [[Potenze di n nei Limiti|Potenze di n →]]
