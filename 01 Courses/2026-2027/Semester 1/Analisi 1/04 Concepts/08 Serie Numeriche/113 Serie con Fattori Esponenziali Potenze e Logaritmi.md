---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 12, PDF pp. 6-10
---

# Serie con fattori esponenziali, potenze e logaritmi

## Quando si usa

Gli esempi del docente mostrano come scegliere fra [[110 Criterio del Rapporto per Serie|rapporto]], [[111 Criterio della Radice per Serie|radice]] e [[108 Serie Armoniche Generalizzate e di Bertrand|serie campione]]. Il fattore esponenziale decide spesso il carattere; quando la base vale $1$, bisogna analizzare i fattori rimasti. I parametri sono fissati mentre $n\to+\infty$.

## Esempio 1 — $\sum a^n/n^n$, con $a\geq0$

### Idea

La radice ennesima elimina entrambe le potenze di esponente $n$.

### Svolgimento passo per passo

Per $n\geq1$ il termine è non negativo e

$$
\sqrt[n]{\frac{a^n}{n^n}}=\frac an\longrightarrow0<1.
$$

Il criterio della radice dà la **convergenza per ogni $a\geq0$**. Per $a=0$ la serie è la serie nulla.

Il PDF risolve anche con il rapporto. Per $a>0$,

$$
\frac{a^{n+1}}{(n+1)^{n+1}}\frac{n^n}{a^n}
=\frac{a}{n+1}\left(\frac{n}{n+1}\right)^n.
$$

Il secondo fattore si può riscrivere

$$
\left(1-\frac1{n+1}\right)^n
=\left(1-\frac1{n+1}\right)^{n+1}
 \left(1-\frac1{n+1}\right)^{-1}
\longrightarrow e^{-1}\cdot1.
$$

Si usano i [[90 Numero di Nepero e Limiti di Tipo Esponenziale|limiti di tipo esponenziale]]. Il rapporto tende quindi a $0\cdot e^{-1}=0$ e conferma la convergenza.

### Cosa imparare

La radice è più breve in questo caso. Per $a=0$ non si usa il rapporto: sarebbe $0/0$, mentre la conclusione sulla serie nulla è immediata dalla definizione.

## Esempio 2 — $\sum n^a b^n$, con $a\in\mathbb R$, $b\geq0$

### Idea e calcolo

Per $b>0$ i termini sono positivi e

$$
\sqrt[n]{n^a b^n}
=b\,n^{a/n}
=b\exp\left(a\frac{\log n}{n}\right)\longrightarrow b.
$$

La [[85 Gerarchia degli Infiniti|gerarchia degli infiniti]] dà $\log n/n\to0$. La potenza di $n$ non cambia il limite della radice.

- Se $0<b<1$, la serie converge per ogni $a$.
- Se $b>1$, la serie diverge a $+\infty$ per ogni $a$; il criterio dà anche $n^a b^n\to+\infty$.
- Se $b=0$, ogni termine è zero, quindi la serie converge per ogni $a$.
- Se $b=1$, la radice tende a $1$ e non decide. La serie diventa $\sum n^a=\sum1/n^{-a}$: converge esattamente quando $-a>1$, cioè $a<-1$.

### Risultato

| Parametri | Carattere |
|---|---|
| $0\leq b<1$, qualunque $a$ | Convergente |
| $b=1$, $a<-1$ | Convergente |
| $b=1$, $a\geq-1$ | Divergente a $+\infty$ |
| $b>1$, qualunque $a$ | Divergente a $+\infty$ |

La soglia $b=1$ va studiata separatamente: non si può trasferire automaticamente la conclusione dai casi vicini.

## Esempio 3 — $\sum a^n(\log n)^b$, con $a>0$, $b\in\mathbb R$

Si parte da $n=2$, così $\log n>0$ e la potenza reale $(\log n)^b$ è definita e positiva.

### Rapporto consecutivo

$$
\frac{a^{n+1}(\log(n+1))^b}{a^n(\log n)^b}
=a\left(\frac{\log(n+1)}{\log n}\right)^b.
$$

Poiché

$$
\frac{\log(n+1)}{\log n}
=1+\frac{\log(1+1/n)}{\log n}\longrightarrow1,
$$

il rapporto tende ad $a$. Ne segue convergenza per $0<a<1$ e divergenza positiva per $a>1$, qualunque sia $b$.

### Il caso $a=1$

Resta $\sum_{n=2}^{+\infty}(\log n)^b$.

- Per $b>0$, il termine tende a $+\infty$: fallisce la [[103 Condizione Necessaria di Convergenza di una Serie|condizione necessaria]].
- Per $b=0$, il termine vale $1$: le somme parziali crescono senza limite.
- Per $b<0$, poniamo $c=-b>0$. Il termine è $1/(\log n)^c\to0$, ma questo non basta. La gerarchia dà $(\log n)^c/n\to0$, quindi definitivamente $(\log n)^c\leq n$. Passando ai reciproci positivi,

$$
\frac1{(\log n)^c}\geq\frac1n.
$$

La [[104 Serie Armonica|serie armonica]] diverge; per [[107 Criterio del Confronto per Serie|confronto]] diverge anche la serie in esame.

### Risultato

$$
\boxed{\sum_{n=2}^{+\infty}a^n(\log n)^b
\text{ converge se e solo se }0<a<1.}
$$

Per $a\geq1$ diverge a $+\infty$, per ogni $b\in\mathbb R$.

## Metodo ed errori comuni

1. Controllare dominio e segno dei termini.
2. Scegliere il criterio che semplifica meglio la dipendenza da $n$.
3. Separare i valori del parametro per i quali il limite è minore, uguale o maggiore di $1$.
4. Nel caso uguale a $1$, tornare alla serie originaria e usare una famiglia campione o un confronto.

Non confondere esponente e parametro della base. Il criterio inconclusivo non prova né convergenza né divergenza. Un termine logaritmico che tende a zero può ancora dare una serie divergente.

### Da dire all'orale

> Rapporto e radice isolano il fattore geometrico. Se il loro limite è uno, devo studiare separatamente il fattore residuo. In particolare, una potenza negativa del logaritmo tende a zero ma la sua serie diverge, perché è definitivamente maggiore del termine della serie armonica.
