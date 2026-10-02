---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 06, PDF pp. 4-5
  - Libro, §2.4.5, pp. 56-59
---

# Funzioni potenza e radice come inversa

## Potenze con esponente naturale

Fissato $m\in\mathbb N$, con $m\geq1$, consideriamo

$$
p_m(x)=x^m.
$$

Il comportamento dipende dalla parità di $m$.

## Esponente dispari

Se $m$ è dispari, la funzione

$$
p_m:\mathbb R\to\mathbb R,
\qquad p_m(x)=x^m,
$$

è strettamente crescente e biiettiva. La sua inversa è la radice $m$-esima:

$$
p_m^{-1}(y)=\sqrt[m]{y},
\qquad y\in\mathbb R.
$$

Una radice di indice dispari è quindi definita anche per argomenti negativi.

## Esponente pari

Se $m$ è pari, su tutto $\mathbb R$ la funzione non è iniettiva, perché

$$
p_m(x)=p_m(-x).
$$

Restringendo il dominio alla semiretta non negativa si ottiene invece la funzione strettamente crescente e biiettiva

$$
p_m:[0,+\infty)\to[0,+\infty),
\qquad p_m(x)=x^m.
$$

La sua inversa è la radice principale:

$$
p_m^{-1}(y)=\sqrt[m]{y},
\qquad y\geq0.
$$

Per esempio, l'inversa di $x\mapsto x^2$ ristretta a $[0,+\infty)$ è $y\mapsto\sqrt y$.

![[66 Funzione Inversa - Simmetria.svg|691]]

## Radice e soluzioni di un'equazione

È importante distinguere l'inversa dalla risoluzione dell'equazione $x^m=y$ su tutto $\mathbb R$:

- se $m$ è dispari, esiste un'unica soluzione reale $x=\sqrt[m]{y}$;
- se $m$ è pari e $y>0$, le soluzioni reali sono $x=\pm\sqrt[m]{y}$;
- la funzione inversa della restrizione a $[0,+\infty)$ restituisce soltanto il ramo non negativo.

### Da dire all'orale

> Per un esponente pari la potenza non è iniettiva su $\mathbb R$. La radice principale nasce come inversa della restrizione della potenza a $[0,+\infty)$.

## Errori comuni

- Affermare che $x^m$ è invertibile su $\mathbb R$ anche quando $m$ è pari.
- Scrivere $\sqrt[m]{y}=\pm r$: il simbolo di radice principale indica un solo valore.
- Dimenticare il dominio $y\geq0$ per una radice reale di indice pari.
- Confondere le soluzioni di un'equazione con i valori di una funzione inversa.

## Connessioni

- Usa [[66 Funzione Inversa|funzione inversa]] e [[67 Monotonia e Funzione Inversa|stretta monotonia]].
- La necessità di restringere il dominio richiama [[65 Funzioni Iniettive e Biiettive|iniettività e biiettività]].
- Generalizza l'esempio delle due restrizioni di $x^2$.

## Prospettiva d'esame

Quando si chiede l'inversa di una potenza, la parità dell'esponente e il dominio assegnato vanno controllati prima di scrivere la formula della radice.
