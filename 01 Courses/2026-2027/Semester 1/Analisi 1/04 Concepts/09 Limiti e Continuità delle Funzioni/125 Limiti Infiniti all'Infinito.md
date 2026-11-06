---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 13, PDF pp. 13-14
  - Libro, §5.2, pp. 138-142
---

# Limiti infiniti all'infinito

## Definizioni metriche nell'ordine del docente

Per $f:I\subseteq\mathbb R\to\mathbb R$, con la direzione considerata di accumulazione per $I$,

$$
\lim_{x\to+\infty}f(x)=+\infty
\iff
\forall M>0\ \exists K>0\ \forall x\in I:
\quad x>K\Longrightarrow f(x)>M.
$$

Analogamente,

$$
\lim_{x\to+\infty}f(x)=-\infty
\iff
\forall M>0\ \exists K>0\ \forall x\in I:
\quad x>K\Longrightarrow f(x)<-M.
$$

Il docente richiama poi i due casi per $x\to-\infty$. Le definizioni complete si ottengono sostituendo la condizione sull'ascissa con $x<-K$:

| Avvicinamento | Limite $+\infty$ | Limite $-\infty$ |
|---|---|---|
| $x\to+\infty$ | $\forall M>0\ \exists K>0:\ x>K\Rightarrow f(x)>M$ | $\forall M>0\ \exists K>0:\ x>K\Rightarrow f(x)<-M$ |
| $x\to-\infty$ | $\forall M>0\ \exists K>0:\ x<-K\Rightarrow f(x)>M$ | $\forall M>0\ \exists K>0:\ x<-K\Rightarrow f(x)<-M$ |

In ogni riga si quantifica soltanto sui punti $x\in I$.

## Esempi del docente

$$
\lim_{x\to-\infty}e^{-x}=+\infty,
\qquad
\lim_{x\to+\infty}\log x=+\infty.
$$

## Commenti: distinguere le due soglie

La lettera $M$ indica quanto chiediamo che il valore della funzione sia grande in modulo. La lettera $K$ indica quanto dobbiamo spostarci sull'asse delle ascisse per garantirlo. L'ordine è **prima $M$, poi la scelta di $K$**, che può dipendere da $M$.

Per l'esempio logaritmico, fissato $M>0$, scegliamo $K=e^M$. Per $x>K$ la monotonia del logaritmo dà $\log x>M$. Per l'esponenziale a $-\infty$, prendiamo $K=\max\{1,\log M\}$: da $x<-K$ segue $-x>K\geq\log M$, dunque $e^{-x}>M$.

## Errori comuni

Una funzione illimitata superiormente non tende necessariamente a $+\infty$. La divergenza richiede che **tutti** i valori nella coda opportuna superino ogni soglia. Per esempio $x\sin x$ è illimitata superiormente a $+\infty$, ma vale zero per $x=n\pi$, quindi non tende a $+\infty$.

Non confondere il segno del punto di avvicinamento con il segno del limite: $e^{-x}$ cresce senza limite quando $x$ tende a $-\infty$.

### Da dire all'orale

> Una funzione tende a più infinito per x tendente a più infinito se, fissata qualsiasi soglia positiva sui valori, esiste una soglia sulle ascisse oltre la quale tutti i valori della funzione la superano. Per il limite meno infinito i valori devono essere inferiori all'opposto della soglia positiva.
