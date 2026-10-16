---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 1, PDF pp. 5-6, pagine stampate 15-16"
---

# Implicazione e contrapposizione

Stato: **da studiare**.

## Implicazione

La scrittura

$$
P\implies Q
$$

afferma che, ogni volta che è vera l'ipotesi $P$, è vera anche la conclusione $Q$.

La conclusione $Q$ è una condizione necessaria per $P$; l'ipotesi $P$ è una condizione sufficiente per $Q$.

## Contrapposizione

Il professore richiama l'equivalenza logica

$$
(P\implies Q)\iff(\neg Q\implies\neg P).
$$

Il simbolo $\neg$ indica la negazione. Per ottenere la contrapposta si negano entrambe le proposizioni e si inverte il verso del ragionamento.

### Perché funziona

Supponiamo vera $P\implies Q$ e supponiamo falsa $Q$. Se $P$ fosse vera, l'implicazione renderebbe vera $Q$, contraddicendo l'ipotesi. Quindi $P$ è falsa.

Viceversa, supponiamo vera $\neg Q\implies\neg P$ e supponiamo vera $P$. Se $Q$ fosse falsa, la contrapposta renderebbe falsa $P$. Quindi $Q$ è vera.

## L'esempio della bicicletta

Il PDF propone:

> Se vado in bicicletta in salita, la frequenza cardiaca aumenta.

Accettando questa implicazione come ipotesi dell'esempio, la sua contrapposta è:

> Se la frequenza cardiaca non aumenta, non sono andato in bicicletta in salita.

L'esempio illustra una struttura logica; non stabilisce una legge fisiologica universale.

## Applicazione alle funzioni

Per un dominio finito:

$$
F\text{ è una funzione da }A\text{ a }B
\implies
\#F=\#A.
$$

La contrapposta è:

$$
\#F\ne\#A
\implies
F\text{ non è una funzione da }A\text{ a }B.
$$

## L'implicazione inversa è diversa

Da $P\implies Q$ non segue in generale $Q\implies P$.

Infatti l'uguaglianza $\#F=\#A$ non garantisce che $F$ sia una funzione: una prima componente può comparire due volte e un'altra non comparire. Il controesempio completo è in [[05 Funzioni]].

Per confutare $P\implies Q$ occorre un caso con $P$ vera e $Q$ falsa. Un caso con $P$ falsa non è un controesempio all'implicazione.

## Da dire all'orale

> Un'implicazione è logicamente equivalente alla propria contrapposta, che si ottiene negando la conclusione e deducendo la negazione dell'ipotesi. Non è in generale equivalente all'implicazione inversa.

## Collegamenti e fonte

- [[05 Funzioni]] e [[07 Iniettività]].
- Fonte: [[GAL 2026-2027 - 20260917 - LEZIONE 1.pdf#page=5|Lezione 1, pp. 5-6, stampate 15-16]]. La dimostrazione dell'equivalenza è esplicitata dal tutor.
