---
course: Algebra Lineare
type: exam-book
status: da studiare
mastery: non verificata
updated: 2026-10-16
---

# Preparazione all'esame di GAL

Stato: **da studiare**.

## Informazioni riportate nella Lezione 0

Fonte: [[GAL 2026-2027 - 20260916 - LEZIONE 0.pdf#page=3|Lezione 0, pp. 3-4]] del 16 settembre 2026. Queste informazioni documentano la presentazione del corso; eventuali aggiornamenti successivi vanno controllati sulla pagina ufficiale.

### Struttura

- Esercizi: 10 quesiti a risposta chiusa e 2 esercizi a risposta aperta; voto massimo indicato 32.
- Teoria: quesiti vari, come definizioni e teoremi; voto massimo indicato 32.
- Pesi del voto finale: 70% esercizi e 30% teoria.

Il PDF non stabilisce qui che la parte teorica sia orale. Durata e materiali consentiti non sono specificati nelle pagine fornite.

### Soglie rappresentate a p. 3

| Intervallo | Indicazione grafica |
|---|---|
| voto almeno $18/32$ | verde |
| voto almeno $16/32$ e inferiore a $18/32$ | giallo |
| voto inferiore a $16/32$ | rosso |

Nel riquadro del voto finale sono indicati verde per voto $>17$ e rosso per voto $\le17$. La pagina non etichetta separatamente ogni fase rispetto ai semafori: non si deducono ulteriori regole di ammissione tra le parti.

### Media e arrotondamento nell'esempio delle matrici

La [[GAL 2026-2027 - 20260930 - LEZIONE 3.pdf#page=2|Lezione 3, p. 2, stampata 22]] presenta:

$$
V(t,e)=\left\lceil0{,}3t+0{,}7e\right\rceil,
$$

con teoria sulle righe ed esercizi sulle colonne. $\lceil x\rceil$ è il più piccolo intero maggiore o uguale a $x$. Nella tabella i risultati oltre 30 sono riportati con 30L.

Questa è la rappresentazione esplicita del materiale, senza aggiungere regole amministrative non riportate.

## Prova in itinere indicata nel PDF

La data riportata a p. 3 è **30 ottobre 2026**.

- 5 quesiti e 1 esercizio.
- Nessuna parte di teoria in quella prova.
- Obiettivo: valutazione formativa dei contenuti della prima parte del corso.
- Effetto soltanto premiale sul voto della parte di esercizi.
- Validità indicata: primo appello invernale al quale lo studente partecipa.

La preparazione degli appunti non viene organizzata automaticamente intorno a questa data.

### Combinazione dei voti

A p. 4:

- $V$ è il voto della prova in itinere;
- $W$ è il voto della parte di esercizi dell'esame completo.

Il voto della parte di esercizi diventa

$$
E=
\begin{cases}
W,&W\ge V,\\[2pt]
\dfrac13V+\dfrac23W,&W<V.
\end{cases}
$$

Quando $W<V$, il valore combinato supera $W$:

$$
\left(\frac13V+\frac23W\right)-W
=\frac{V-W}{3}>0.
$$

Quest'ultimo passaggio del tutor chiarisce l'effetto premiale.

Esempi del professore:

$$
V=23,\quad W=27
\quad\Longrightarrow\quad E=27;
$$

$$
V=23,\quad W=21
\quad\Longrightarrow\quad
E=\frac{23+42}{3}=\frac{65}{3}\approx21{,}67.
$$

Si tratta del voto combinato della parte di esercizi prima di eventuali passaggi successivi, non del voto finale comprensivo della teoria.

## Definizioni da studiare

- [[01 Prodotto Cartesiano]] e [[02 Relazioni Binarie]].
- [[03 Relazioni di Equivalenza]] e [[04 Relazioni di Ordine]].
- [[05 Funzioni]], [[07 Iniettività]], [[08 Suriettività]], [[09 Biiettività]].
- [[10 Prodotti Cartesiani di Più Insiemi]].
- [[11 Matrici come Funzioni e Indici]] e [[12 Campi Numerici e Campo F2]].

## Proprietà e ragionamenti

- [[06 Implicazione e Contrapposizione]].
- Dimostrazione dell'ordine per inclusione.
- Biiezione tra coppie annidate e terne.
- [[13 Uguaglianza e Somma di Matrici|Somma, matrice nulla e opposta]].
- [[14 Prodotto di una Matrice per uno Scalare|Prodotto per scalare e proprietà]].
- [[15 Proprietà e Costo dei Calcoli Matriciali|Conteggio delle operazioni]].

Sono risultati pertinenti ai PDF, senza classificare automaticamente ogni dimostrazione come obbligatoria all'esame.

## Formule e condizioni

| Formula | Condizioni |
|---|---|
| $\#(A\times B)=\#A\,\#B$ | insiemi finiti |
| $F(a_1)=F(a_2)\Rightarrow a_1=a_2$ | criterio di iniettività per una funzione |
| $\forall b\in B,\ \exists a\in A:F(a)=b$ | criterio di suriettività rispetto al codominio dichiarato |
| $(A+B)_{ij}=a_{ij}+b_{ij}$ | stesso campo e stesse dimensioni |
| $(\lambda A)_{ij}=\lambda a_{ij}$ | $\lambda\in\mathbb K$, $A\in M_{\mathbb K}(m,n)$ |
| $\lambda(A+B)=\lambda A+\lambda B$ | matrici dello stesso tipo |
| $1+1=0$ | operazione in $\mathbb F_2$ |

## Argomenti delle lezioni 4 6 e 7

Stato: **da studiare**. Sono contenuti dei PDF, senza aggiungere obblighi d'esame non verificati.

- [[16 Prodotto Matriciale Righe per Colonne]] e [[17 Prodotto Matriciale e Composizione]].
- [[18 PageRank e Matrici di Transizione]] come applicazione.
- [[19 Proprietà del Prodotto e Matrice Identità]] e [[20 Matrici Invertibili]].
- [[21 Rango e Prodotti Colonna per Riga]] e [[27 Calcolo del Rango con Gauss]].
- [[22 Determinante e Sviluppo di Laplace]] e [[23 Matrici Diagonali e Triangolari]].
- [[24 Operazioni Elementari e Metodo di Gauss]], [[25 Pivot e Matrici a Scala]], [[26 Matrici Elementari e Reversibilità del MEG]].
- [[28 Teorema di Binet e Proprietà del Determinante]], [[29 Calcolo del Determinante con Gauss]].

### Formule con condizioni

| Risultato | Condizioni |
|---|---|
| $c_{ij}=\sum_k a_{ik}b_{kj}$ | $A:m\times n$, $B:n\times p$; risultato $m\times p$ |
| $AI_n=I_mA=A$ | $A:m\times n$ |
| $r(A)=\text{numero dei pivot di }U$ | $U$ a scala ottenuta con operazioni elementari |
| $\det T=\prod_i t_{ii}$ | $T$ triangolare quadrata |
| $\det(AB)=\det A\det B$ | matrici quadrate dello stesso ordine |
| $\det(\lambda A)=\lambda^n\det A$ | $A:n\times n$ |
| $\det A\ne0\iff r(A)=n\iff A\text{ invertibile}$ | $A:n\times n$ su un campo |

Per Gauss sul determinante, registrare gli scambi e i riscalamenti: soltanto la somma di un multiplo di un'altra riga conserva sempre il valore. Per i prodotti si conservano ordine dei fattori e dimensioni.

Le dimostrazioni delle nuove note chiariscono due condizioni: non si cancella una matrice arbitraria da un prodotto; in $\mathbb F_2$ non si divide per 2.

## Argomenti delle lezioni 9 10 e 11

Stato: **da studiare**. Questi sono argomenti dei nuovi PDF, non un elenco di obblighi d'esame aggiuntivi.

- [[30 Sistemi Lineari e Rappresentazioni Matriciali]], [[31 Risoluzione dei Sistemi con Gauss e Parametri]].
- [[32 Teorema di Rouché-Capelli]]: enunciato, dimostrazione e numero di parametri.
- [[33 Nucleo e Struttura delle Soluzioni]]: Teorema 10.1 e doppia inclusione.
- [[34 Teorema di Cramer e Soluzione Unica]]: enunciato del PDF e formula dei determinanti come integrazione.
- [[35 Ricerca della Matrice Inversa con Gauss]]: più termini noti, inverse laterali e Teorema 10.3.
- [[36 Spazi Affini ed Equazioni Cartesiane e Parametriche]], [[37 Rette e Piani tra Parametri e Vincoli]].
- [[38 Spazi Vettoriali e Assiomi]], [[39 Esempi di Spazi Vettoriali]].
- [[40 Proprietà Elementari degli Spazi Vettoriali]], [[41 Sottospazi Vettoriali e Criterio di Chiusura]].

### Risultati con condizioni

| Risultato | Condizioni |
|---|---|
| $Ax=b$ compatibile $\iff r(A)=r([A\mid b])$ | $A:m\times n$, $b\in\mathbb K^m$ |
| Numero di parametri liberi $=n-r(A)$ | sistema compatibile, parametrizzazione non ridondante |
| Numero di soluzioni $=q^{n-r(A)}$ | sistema compatibile su un campo finito con $q$ elementi |
| $\{x:Ax=b\}=P+\ker(A)$ | $P$ deve essere una soluzione particolare |
| Unica soluzione per ogni $b$ | $A:n\times n$ di rango $n$ |
| $x_j=\det A_j(b)/\det A$ | $A$ quadrata, $\det A\ne0$; integrazione dimostrata del tutor |
| $[A\mid I]\longrightarrow[I\mid A^{-1}]$ | $A$ quadrata invertibile; operazioni su entrambi i blocchi |
| Una retta richiede $n-1$ vincoli non ridondanti | retta autentica in $\mathbb R^n$, direzione non nulla |
| Un piano richiede $n-2$ vincoli non ridondanti | $n\ge2$, due direzioni indipendenti |
| $0\in H$, $H+H\subseteq H$, $\lambda H\subseteq H$ per ogni $\lambda$ | criterio di sottospazio di un ambiente vettoriale fissato |

Prima di dividere per un'espressione con parametri, separare il caso in cui si annulla. Nella verifica dei sottospazi lo zero è necessario ma non sufficiente; servono entrambe le chiusure.

## Esempi e stato personale

- [[01 Prodotti Cartesiani e Relazioni]].
- [[02 Esempi Svolti sulle Funzioni]].
- [[03 Esempi Svolti sulle Matrici]].
- [[04 Prodotto Composizione e Navigazione]].
- [[05 Rango Laplace e Matrici Triangolari]].
- [[06 Gauss Rango Determinante e Inversa]].

- [[07 Sistemi Lineari Gauss e Rouché-Capelli]].
- [[08 Nucleo Struttura Cramer e Inverse]].
- [[09 Spazi Vettoriali Sottospazi e Geometria]].

Tutti gli esempi sono **da studiare** e preparati dal tutor. Nessun esercizio autonomo, errore personale verificato o simulazione è registrato. Gli errori frequenti delle note sono avvertenze didattiche generali.
