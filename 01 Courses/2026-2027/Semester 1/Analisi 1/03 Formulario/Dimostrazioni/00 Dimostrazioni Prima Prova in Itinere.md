---
course: Analisi 1
type: exam-index
exam: Prima prova in itinere
status: Da studiare
updated: 2026-10-30
source:
  - "AM1-regolamento26-27.pdf, pp. 1-2"
  - "AM1 L12 26-27.pdf, p. 30: fine argomenti della prima prova in itinere"
  - "Lezioni 01-12 e note dei concetti 1-118"
cssclasses:
  - formulario
---

# Teoremi e dimostrazioni della prima prova in itinere

[[00 Indice Formulario|Indice del Formulario]] · [[02 Exam Book|Exam Book]] · [[00 Indice dei Concetti|Concetti del corso]]

## Fonti e programma

Il [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2, elenca le dimostrazioni richieste per lo scritto dell’intero corso. Il docente chiude gli argomenti della **prima prova in itinere** a p. 30 del PDF della [[Lecture 12]]. All’interno di questo programma rientrano le voci **D1–D14**, dalla radice di due alla convergenza assoluta delle serie.

Il regolamento, p. 1, precisa che anche gli altri teoremi del programma possono essere chiesti come **enunciato, comprensione o applicazione**. Per questo la raccolta comprende sia le 14 dimostrazioni complete sia quattro riepiloghi degli altri risultati.

## Dimostrazioni richieste: D1–D14

Ogni scheda contiene **enunciato e ipotesi, idea della prova, dimostrazione completa e punti da ricordare**. I numeri D seguono l’elenco ufficiale.

| Voce | Scheda completa                                                                                              | Passaggio chiave                                      |
| ---- | ------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------- |
| D1   | [[D01 Irrazionalità della Radice di Due\|Irrazionalità della Radice di Due]]                                 | Assurdo, frazione ridotta e parità                    |
| D2   | [[D02 Disuguaglianza di Bernoulli\|Disuguaglianza di Bernoulli]]                                             | Induzione e termine $nx^2\geq0$                       |
| D3   | [[D03 Formule di De Moivre per Prodotti e Potenze\|Formule di De Moivre per Prodotti e Potenze]]             | Formule di addizione; induzione sulle potenze         |
| D4   | [[D04 Radici Ennesime di un Numero Complesso\|Radici Ennesime di un Numero Complesso]]                       | Moduli e argomenti; elenco completo e radici distinte |
| D5   | [[D05 Unicità del Limite\|Unicità del Limite]]                                                               | Intorni disgiunti e massimo delle soglie              |
| D6   | [[D06 Limitatezza delle Successioni Convergenti\|Limitatezza delle Successioni Convergenti]]                 | Fascia con $\varepsilon=1$ e primi termini            |
| D7   | [[D07 Teorema di Permanenza del Segno\|Teorema di Permanenza del Segno]]                                     | $\varepsilon=\lvert\ell\rvert/2$; casi infiniti       |
| D8   | [[D08 Teorema dei Due Carabinieri\|Teorema dei Due Carabinieri]]                                             | Stessa fascia e massimo di tre soglie                 |
| D9   | [[D09 Regolarità delle Successioni Monotone\|Regolarità delle Successioni Monotone]]                         | Supremo o infimo e monotonia; casi illimitati         |
| D10  | [[D10 Condizione Necessaria di Convergenza di una Serie\|Condizione Necessaria di Convergenza di una Serie]] | $a_N=S_N-S_{N-1}$                                     |
| D11  | [[D11 Teorema del Confronto per le Serie\|Teorema del Confronto per le Serie]]                               | Confronto delle somme parziali non negative           |
| D12  | [[D12 Teorema del Confronto Asintotico per le Serie\|Teorema del Confronto Asintotico per le Serie]]         | $b_n/2<a_n<3b_n/2$                                    |
| D13  | [[D13 Criterio del Rapporto per le Serie Numeriche\|Criterio del Rapporto per le Serie Numeriche]]           | Maggiorante o minorante geometrico                    |
| D14  | [[D14 Convergenza Assoluta Implica Convergenza Semplice\|Convergenza Assoluta Implica Convergenza Semplice]] | $0\leq a_n+\lvert a_n\rvert\leq2\lvert a_n\rvert$     |

## Altri enunciati da conoscere

Queste note raccolgono gli altri teoremi, corollari e formule del programma, con le ipotesi necessarie. Le prove D già elencate sono richiamate tramite collegamenti.

1. [[Enunciati 01 Numeri Reali Complessi e Funzioni]] — completezza, estremi, triangolare, densità, radici reali, proprietà algebriche, teorema fondamentale dell’algebra e funzioni inverse.
2. [[Enunciati 02 Successioni e Limiti]] — algebra e confronto dei limiti, limitata per infinitesima, geometriche, rapporto per successioni, aritmetizzazione dell’infinito e potenze variabili.
3. [[Enunciati 03 Equivalenti e Limiti Notevoli]] — numero di Nepero, gerarchia, o-piccolo, equivalenti, sviluppi notevoli e cautele con logaritmi ed esponenti variabili.
4. [[Enunciati 04 Serie Numeriche]] — geometriche, linearità, code, telescopiche, regolarità, armoniche e Bertrand, radice, Stirling, convergenza assoluta e Leibniz.

Il **criterio della radice** e il **criterio di Leibniz** sono inclusi negli enunciati. Le loro dimostrazioni non sono nell’elenco D1–D14 dello scritto; la prova didattica eventualmente presente nei concetti resta consultabile dalle note di riferimento.

## Come ripetere una dimostrazione

1. Enuncia il risultato indicando **tutte le ipotesi** e distinguendole dalla tesi.
2. Spiega in una frase l’idea della prova.
3. Ricostruisci i passaggi e motiva le scelte di $\varepsilon$, delle soglie o dei confronti.
4. Controlla i casi finiti e infiniti previsti dall’enunciato.
5. Ricorda un controesempio quando il viceversa è falso o quando un’ipotesi è indispensabile.

Per confrontare i valori e le motivazioni delle tolleranze usate nelle prove: [[Scelta di Epsilon nelle Dimostrazioni]].

## Controesempi essenziali

- **Limitata non implica convergente:** $(-1)^n$.
- **Convergente non implica monotona:** $(-1)^n/n$.
- **Termini positivi non implicano limite positivo:** $1/n\to0$.
- **Termine infinitesimo non implica serie convergente:** la serie armonica.
- **Rapporto o radice con limite $1$ non decidono:** $\sum1/n$ diverge, $\sum1/n^2$ converge.
- **Convergenza semplice non implica assoluta:** l’armonica alternata.
- **Equivalenti non si sottraggono automaticamente:** $1+1/n\sim1+1/n^2$, ma $1/n\not\sim1/n^2$.

Per le definizioni e gli esercizi completi: [[00 Indice Formulario]] e le note dei concetti collegate nelle singole schede.
