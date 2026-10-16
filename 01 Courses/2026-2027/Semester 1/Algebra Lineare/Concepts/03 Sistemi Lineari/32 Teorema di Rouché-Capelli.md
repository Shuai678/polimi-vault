---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 9, PDF pp. 6-9, stampate 78-81"
---

# Teorema di Rouché-Capelli

Stato: **da studiare**.

## Domanda centrale

La matrice $A$ contiene i coefficienti; $[A\mid b]$ aggiunge il vincolo imposto dai termini noti. Il confronto tra i ranghi stabilisce se questi vincoli possono essere soddisfatti insieme.

## Enunciato del Teorema 9.1

Siano $A\in M_{\mathbb K}(m,n)$ e $b\in\mathbb K^m$. Allora

$$
\boxed{Ax=b\text{ è risolubile}\iff r(A)=r([A\mid b]).}
$$

Se il rango comune è $r$, esistono $v_0,v_1,\ldots,v_{n-r}\in\mathbb K^n$ tali che tutte e sole le soluzioni sono

$$
\boxed{x=v_0+t_1v_1+\cdots+t_{n-r}v_{n-r},
\qquad t_1,\ldots,t_{n-r}\in\mathbb K.}
$$

Nella costruzione con Gauss i parametri sono i valori delle variabili libere; quindi sono $n-r$, non $m-r$. $v_0$ è una soluzione particolare.

## Strategia della dimostrazione

Ridurre a scala la matrice completa. Il rango conta i pivot; l'esistenza di un pivot nella colonna dei termini noti equivale a un'equazione impossibile. Nel caso compatibile, la sostituzione all'indietro produce la parametrizzazione.

## Dimostrazione del criterio

Con le stesse operazioni di riga otteniamo

$$
[A\mid b]\longrightarrow[U\mid c],\qquad U=TA,\quad c=Tb,
$$

dove $T$ è invertibile. Le operazioni conservano i ranghi e l'insieme delle soluzioni. Sia $r=r(U)=r(A)$.

Le prime $r$ righe di $U$ sono non nulle e hanno pivot; le rimanenti sono nulle.

### Caso A: tutti i termini noti delle righe nulle sono zero

Le righe sotto la $r$-esima sono interamente nulle anche nella matrice completa. Non compare un pivot aggiuntivo, perciò

$$
r([A\mid b])=r([U\mid c])=r.
$$

Assegnando valori arbitrari alle variabili libere, si risolvono le $r$ equazioni rimaste dal basso verso l'alto. Ogni divisione è per un pivot non nullo. Il sistema è risolubile.

### Caso B: almeno una riga nulla di $U$ ha termine noto non nullo

Quella riga impone $0=c_i\ne0$. Il sistema è impossibile.

Le righe della forma $(0,\ldots,0,c_i)$ non nulle sono tutte multipli l'una dell'altra: producono **un solo** pivot aggiuntivo nella colonna finale. Dunque

$$
r([A\mid b])=r+1>r(A).
$$

I due casi esauriscono le possibilità e dimostrano entrambe le implicazioni.

## Dimostrazione della forma delle soluzioni

Siano $f_1,\ldots,f_{n-r}$ gli indici delle colonne senza pivot. Poniamo $x_{f_\ell}=t_\ell$.

La sostituzione all'indietro usa somme, prodotti per coefficienti fissati e divisioni per pivot fissati. Quindi ciascuna coordinata pivot è una costante più una combinazione lineare dei parametri:

$$
x_j=\alpha_{j0}+\sum_{\ell=1}^{n-r}\alpha_{j\ell}t_\ell.
$$

Raggruppando le costanti in $v_0$ e i coefficienti di ogni $t_\ell$ in $v_\ell$ si ottiene la formula dell'enunciato.

Nelle coordinate libere:

$$
(v_0)_{f_i}=0,\qquad
(v_\ell)_{f_i}=
\begin{cases}1,&i=\ell,\\0,&i\ne\ell.\end{cases}
$$

Di conseguenza parametri diversi danno soluzioni diverse: basta guardare le coordinate libere. La costruzione non perde alcuna soluzione perché ogni soluzione possiede proprio quei valori delle coordinate libere.

Se $\sum_\ell t_\ell v_\ell=0$, guardare la coordinata $f_i$ dà $t_i=0$ per ogni $i$. Questo spiega anche la non ridondanza delle direzioni, senza presupporre ancora la teoria delle basi.

## Come leggere correttamente il risultato

| Situazione | Conclusione |
|---|---|
| $r([A\mid b])=r(A)+1$ | nessuna soluzione |
| $r([A\mid b])=r(A)=n$ | una sola soluzione |
| $r([A\mid b])=r(A)=r<n$ | $n-r$ parametri liberi |

Nell'ultima riga le soluzioni sono infinite solo se il campo è infinito.

Il numero delle equazioni, da solo, non determina esistenza o unicità. Un sistema con più equazioni che incognite può avere una soluzione se alcune equazioni sono ridondanti; un sistema con meno equazioni che incognite può essere impossibile.

### Caso limite del tutor

Se $A=0$, allora $r(A)=0$. Se anche $b=0$, ogni $x\in\mathbb K^n$ è soluzione; se $b\ne0$, il rango della completa è 1 e non esiste soluzione.

## Da dire all'orale

> Un sistema è compatibile se e solo se il rango della matrice dei coefficienti coincide con quello della completa. Se il rango comune è $r$, Gauss individua $r$ variabili pivot e $n-r$ variabili libere; le soluzioni sono un vettore particolare più una combinazione di $n-r$ direzioni.

## Collegamenti e fonte

- [[27 Calcolo del Rango con Gauss]], [[30 Sistemi Lineari e Rappresentazioni Matriciali]], [[31 Risoluzione dei Sistemi con Gauss e Parametri]].
- [[33 Nucleo e Struttura delle Soluzioni]], [[34 Teorema di Cramer e Soluzione Unica]].
- [[GAL 2026-2027 - 20261012 - LEZIONE 9.pdf#page=6|Lezione 9, pp. 6-9, stampate 78-81]].
