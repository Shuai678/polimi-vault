---
course: Analisi 1
type: exam-book
updated:
---

# Exam Book

## Exam Information

- Format: TBD
- Date: TBD
- Duration: TBD
- Allowed material: TBD

## Formula Sheet

- No formulas recorded yet.

## Formula Conditions

- Record when each formula applies, required hypotheses, and when not to use it.
- Per usare le forme $n=2k$ e $n=2k+1$, il numero $n$ deve essere intero e $k$ deve essere un intero opportuno.
- In un campo, l'inverso moltiplicativo $a^{-1}$ è richiesto soltanto per $a\neq0$; lo zero non è invertibile.
- Moltiplicando una disuguaglianza per un fattore positivo il verso resta invariato; per un fattore negativo si inverte; per un fattore nullo entrambi i membri diventano zero.
- Per negare la limitatezza superiore di $E$ bisogna mostrare che $\forall k$ esiste $x\in E$ tale che $x>k$; analogamente per la limitatezza inferiore.
- Per verificare $x_0=\max E$ occorrono entrambe le condizioni: $x_0\in E$ e $x\leq x_0$ per ogni $x\in E$. Analogamente per il minimo.
- $\sup E$ è il minimo dei maggioranti e $\inf E$ è il massimo dei minoranti; non devono appartenere a $E$.
- Se $\sup E\in E$, allora coincide con $\max E$; analogamente, se $\inf E\in E$, coincide con $\min E$.
- Completezza di $\mathbb{R}$: ogni sottoinsieme non vuoto e limitato superiormente possiede estremo superiore; equivalentemente per l'estremo inferiore.
- Caratterizzazione del superiore: verificare che $s$ sia un maggiorante e che, per ogni $k<s$, esista $x\in E$ con $k<x\leq s$.
- Valore assoluto: per $r\geq0$, $|x|\leq r$ equivale a $-r\leq x\leq r$, mentre $|x|>r$ equivale a $x<-r$ oppure $x>r$.
- Disuguaglianza triangolare: $|x+y|\leq|x|+|y|$ per ogni $x,y\in\mathbb{R}$.
- Negli intervalli, una parentesi quadra include l'estremo finito e una parentesi tonda lo esclude; accanto a $\pm\infty$ si usa sempre la parentesi tonda.
- Densità di $\mathbb{Q}$ in $\mathbb{R}$: se $x,y\in\mathbb{R}$ e $x<y$, esiste $r\in\mathbb{Q}$ tale che $x<r<y$.
- Per $y\geq0$ e $n\in\mathbb{N}$ positivo, $\sqrt[n]{y}$ è l'unica soluzione non negativa di $x^n=y$.
- Per ogni $a\in\mathbb{R}$, $\sqrt{a^2}=|a|$.
- Per $a>0$ e $r=\frac mn\in\mathbb{Q}$ con $n>0$, $a^r=\sqrt[n]{a^m}$; se $r<0$, si prende il reciproco.
- Per $a>1$ e $b\in\mathbb{R}$, $a^b$ è definito come $\sup\{a^r:r\in\mathbb{Q},\ r<b\}$; la base deve essere positiva nella definizione generale.

## Problem Types

- Dimostrazioni dirette sulla parità: tradurre l'ipotesi con la definizione e trasformare la quantità della tesi nella forma $2h$ oppure $2h+1$.
- Confutazione di implicazioni universali: trovare un elemento del dominio che renda vera l'ipotesi e falsa la tesi.
- Dimostrazioni per assurdo: assumere la negazione della tesi, dedurre una contraddizione e concludere che la tesi è vera.
- Dimostrazioni per induzione: formulare $P(n)$, verificare il caso base, assumere $P(n)$ e dimostrare $P(n+1)$.

## Typical Mistakes

- Ripetere la forma dell'ipotesi invece di dimostrare la tesi: $n=2k+1$ mostra che $n$ è dispari, mentre per dimostrare che $n^2$ è dispari occorre ottenere $n^2=2h+1$.
- Proporre come controesempio un elemento che rende falsa la tesi ma non soddisfa l'ipotesi.
- Invertire il passo induttivo assumendo $P(n+1)$ e cercando di dimostrare $P(n)$.
- Confondere l'opposto con l'inverso moltiplicativo: $-a$ riguarda la somma, mentre $a^{-1}$ riguarda il prodotto.
- Affermare che $\mathbb{Z}$ non è un campo perché mancano gli opposti; in realtà mancano gli inversi moltiplicativi di molti elementi non nulli.
- Omettere il caso del fattore nullo nel descrivere la moltiplicazione di una disuguaglianza.
- Usare la positività di $i^2$ senza dichiarare la supposizione per assurdo che $\mathbb{C}$ possieda un ordine compatibile.
- Affermare che un insieme non ha maggioranti senza partire da un candidato arbitrario e costruire un elemento che lo superi.
- Verificare che un candidato sia maggiorante o minorante senza controllare che appartenga all'insieme.
- Confondere l'assenza del minimo con l'assenza dell'estremo inferiore.
- Confondere un maggiorante qualsiasi con l'estremo superiore o richiedere che l'estremo appartenga all'insieme.
- Applicare la completezza senza verificare non vacuità, limitatezza e ambiente $\mathbb{R}$.
- Confondere “$E$ è limitato superiormente” con “il candidato $s$ è un maggiorante”.
- Nella caratterizzazione del superiore, scegliere un elemento che non appartiene all'insieme.
- Eliminare le barre del valore assoluto senza controllare il segno o scambiare la congiunzione interna con la disgiunzione esterna.
- Sostituire la disuguaglianza triangolare con l'uguaglianza $|x+y|=|x|+|y|$ senza controllare i segni.
- Confondere massimo con estremo superiore nella lettura di un intervallo o includere simbolicamente $\pm\infty$.
- Enunciare la densità senza l'ipotesi $x<y$ o confonderla con la completezza.
- Confondere $\sqrt[4]{16}=2$ con le due soluzioni $x=\pm2$ dell'equazione $x^4=16$.
- Interpretare $a^{m/n}$ come $a^m/a^n$ o dimenticare il reciproco con esponente negativo.
- Definire potenze con esponente reale senza imporre $a>0$ o confondere il ruolo della densità con quello della completezza.

## Trap List

- Controllare il dominio: “pari” e “dispari” si riferiscono agli interi, non genericamente ai numeri reali.
- Prima di accettare un controesempio, controllare nell'ordine: appartenenza al dominio, verità dell'ipotesi, falsità della tesi.
- In una prova per assurdo indicare esplicitamente sia la supposizione iniziale sia le due affermazioni che costituiscono la contraddizione.
- Nel passo induttivo $P(n)$ è l'ipotesi da assumere, mentre $P(n+1)$ è la tesi da dimostrare.
- Per verificare se un insieme è un campo non basta la chiusura rispetto a somma e prodotto: occorre controllare anche opposti, inversi e tutte le altre proprietà.
- Se la disuguaglianza iniziale è stretta, moltiplicando per zero si ottiene un'uguaglianza e si perde la stretta disuguaglianza.
- Un maggiorante non deve appartenere all'insieme; l'appartenenza diventa invece essenziale nella definizione di massimo.
- La limitatezza è necessaria ma non sufficiente per l'esistenza di massimo o minimo.
- In $\mathbb{R}$ la limitatezza e la non vacuità garantiscono gli estremi superiore e inferiore, ma non massimo e minimo.
- La proprietà dell'estremo superiore non vale in $\mathbb{Q}$; il controesempio fondamentale usa i razionali non negativi con quadrato minore o uguale a $2$.
- La seconda condizione della caratterizzazione deve produrre un elemento valido dell'insieme per ogni soglia inferiore al candidato.

## Wrong Answers Log

- Add links to mistake notes or summarize recurring mistakes.

## Past Exam Observations

- None recorded yet.

## Final Review Checklist

- [ ] Can state core definitions.
- [ ] Can explain formula conditions.
- [ ] Can solve representative exercises without notes.
- [ ] Reviewed repeated mistakes.
