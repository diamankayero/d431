---
title: "Sommes de Riemann"
---

### Sommes de Riemann

#### Définition.

Soit $f$ une fonction définie sur $[a,b]$. Pour toute subdivision $\sigma$ $=(a_0, \cdots, a_n)$ et pour tout $c_0,\cdots,c_{n-1}$ tels que $c_i \in [a_i,a_{i+1}]$,

la somme $\sum_{i=0}^{n}(a_{i+1}-a_i)f(c_i)$ est une somme de Riemann associée à f, à la subdivision $\sigma$ et à $c_i$.

#### Remarque.

On note $\sigma_{n}$ la subdivision de $[a,b]$ de pas $\frac{b-a}{n}$. La somme $$S(f,\sigma_{n})=\sum_{i=1}^{n}\frac{b-a}{n}f(a+i\frac{b-a}{n})$$ est une somme de Riemann associée à f et à la subdivision $\sigma_{n}$.

#### Théorème.

Soit $f$ une fonction continue sur $[a,b]$. Alors, pour toute fammille

$$\lim_{n \to +\infty}\sum_{i=0}^{n-1}\frac{b-a}{n}f(a+i\frac{b-a}{n})= \int_{a}^{b} f\ .$$

::: exercise-box
**Énoncé 1**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\sum_{k=1}^{n} \frac{1}{k+n}$$

<details>

<summary><strong>Corrigé</strong></summary>

Posons $x_n = \sum_{k=1}^{n} \frac{1}{k+n}$ , donc $$\sum_{k=1}^{n} \frac{1}{n(\frac{k}{n}+1)} = \frac{1}{n}\sum_{k=1}^{n}\frac{1}{\frac{k}{n}+1}$$

avec $f(t)$ =$\frac{1}{1+t}$ sur $[0,1]$, on reconnait la somme de Riemann et la subdivision régulière est $\sigma_{n}^{k}$ = $\frac{k}{n}$, $k \in \{1, \dots, n\}$.

Comme $f$ est continue sur $[0,1]$, donc elle est intégrable au sens de Riemann sur $[0,1]$.

La limite est donc $$\lim_{n \to +\infty} x_n = \int_{0}^{1} f(t) \, dt = \int_{0}^{1}\frac{1}{1+t}\,dt = [ \ln(1+t) ]_{0}^{1} = \ln2$$

</details>
:::

::: exercise-box
**Énoncé 2**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\frac{1}{n^2} \left(\sqrt{1(n-1)} + \sqrt{2(n-2)} + \cdots + \sqrt{(n-1)1}\right)$$

<details>

<summary><strong>Corrigé</strong></summary>

Posons $$c_n = \frac{1}{n^2} \left(\sqrt{1(n-1)} + \sqrt{2(n-2)} + \cdots + \sqrt{(n-1)1}\right)$$ En factorisant, on remarque que $$c_n = \frac{1}{n} \sum_{k=1}^{n-1}\sqrt{ \frac{k}{n}(1-\frac{k}{n})} $$

Ainsi, $f(t) = \sqrt{t(1-t)}$ sur $[0,1]$, on reconnait la somme de Riemann et la subdivision régulière est $\sigma_{n}^{k}$ = $\frac{k}{n}$, $k \in \{1, \dots, n\}$.

Comme $f$ est continue sur $[0,1]$, elle est intégrable au sens de Riemann sur $[0,1]$.

La limite est donc $$\lim_{n \to +\infty} c_n = \int_{0}^{1} f(t) \, dt = \int_{0}^{n} \sqrt{t(1-t)}$$

Rappel : $$t(1-t) = t-t^2 = \frac{1}{4}-(t-\frac{1}{2})^2 = \frac{1}{4}(1-(2t-1)^2 )$$

En effectuant un changement de variable, $2t-1 =$ $\sin{y}$, on obtient :

$$ c_n = \frac{1}{8}\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} (\cos(2y)+1)dy = \frac{\pi}{8}$$

</details>
:::

::: exercise-box
**Énoncé 3**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$n \sqrt{(1 + \frac{1}{n})(1 + \frac{2}{n}) \cdots (1 + \frac{n}{n})}$$

<details>

<summary><strong>Corrigé</strong></summary>

Indication:

On applique $\ln$ et après on reconnait la fonction $f$

</details>
:::

::: exercise-box
**Énoncé 4**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\frac{\pi}{n} \left(\sin\left(\frac{\pi}{n}\right) + \sin\left(\frac{2\pi}{n}\right) + \cdots + \sin\left(\frac{(n-1)\pi}{n}\right)\right)$$

<details>

<summary><strong>Corrigé</strong></summary>

Soit $$d_n = \frac{\pi}{n} \left(\sin\left(\frac{\pi}{n}\right) + \sin\left(\frac{2\pi}{n}\right) + \cdots + \sin\left(\frac{(n-1)\pi}{n}\right)\right)$$

donc, $$d_n = \frac{\pi}{n}\sum_{k=0}^{n-1}\sin(\frac{k}{n}\pi)$$ Avec, $f(t) = \sin(t)$ sur $[0,\pi]$, on reconnait la somme de Riemann et la subdivision régulière est $\sigma_{n}^{k}$ = $\frac{k}{n}$, $k \in \{1, \dots, n\}$. Comme $f$ est continue sur $[0,\pi]$, donc elle est intégrable au sens de Riemann sur $[0,\pi]$.

La limite est donc $$\lim_{n \to +\infty} d_n = \int_{0}^{\pi} f(t) \, dt = \int_{0}^{\pi}\sin(t)\,dt = [ -\cos(t) ]_{0}^{\pi} = 2$$

</details>
:::

::: exercise-box
**Énoncé 5**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\frac{\sum_{k=1}^{n}k^{a-1}}{n^a}, \quad a \ge 1$$

<details>

<summary><strong>Corrigé</strong></summary>

Posons $$ e_n = \frac{\sum_{k=1}^{n}k^{a-1}}{n^a}, \quad a \ge 1$$

Alors $$ e_n =\sum_{k=1}^{n}\frac{k^{a-1}}{n^a} = \frac{1}{n}\sum_{k=1}^{n}\frac{k^{a-1}}{n^{a-1}} = \frac{1}{n}\sum_{k=1}^{n} \left(\frac{k}{n} \right)^{a-1}$$

avec $f(t) = t^{a-1}$ sur $[0,1]$, on reconnait la somme de Riemann et la subdivision régulière est $\sigma_{n}^{k}$ = $\frac{k}{n}$, $k \in \{1, \dots, n\}$.

Comme $f$ est continue sur $[0,1]$, elle est intégrable au sens de Riemann sur $[0,1]$.

La limite est donc $$\lim_{n \to +\infty} e_n = \int_{0}^{1} f(t) \, dt = \int_{0}^{1}t^{a-1}\,dt= \frac{1}{a}$$

</details>
:::

::: exercise-box
**Énoncé 6**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\sin\left(\frac{\pi}{n}\right) \sum_{k=0}^{n-1} \frac{1}{2 + \cos\left(\frac{k \pi}{n}\right)}$$

<details>

<summary><strong>Corrigé</strong></summary>

<!-- Insère la solution ici -->

Indication:

Il faut donner une équivalence de $\sin$

</details>
:::

::: exercise-box
**Énoncé 7**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\frac{1}{n^3} \sum_{k=1}^{n} k^2 \sin\left(\frac{k \pi}{n}\right)$$

<details>

<summary><strong>Corrigé</strong></summary>

<!-- Insère la solution ici -->

Posons $$
f_n = \frac{1}{n^3} \sum_{k=1}^{n} k^2 \sin\left(\frac{k \pi}{n}\right)
$$

Alors $$
f_n = \frac{1}{n} \sum_{k=1}^{n} \frac{k^2}{n^2} \sin\left(\frac{k \pi}{n}\right) = \frac{1}{\pi^3} \frac{\pi}{n} \sum_{k=1}^{n} \left(\frac{k\pi}{n}\right)^2 \sin\left(\frac{k \pi}{n}\right)
$$

Avec $f(t) = t^2 \sin(t)$ sur $[0, \pi]$, on reconnaît la somme de Riemann, et la subdivision régulière est $$
\sigma_{n}^{k} = \frac{k}{n}, \quad k \in \{1, \dots, n\}.
$$

Comme $f$ est continue sur $[0, \pi]$, elle est donc intégrable au sens de Riemann sur $[0, \pi]$.

Finalement, nous avons $$
\lim_{n \to +\infty} f_n = \frac{1}{\pi^3} \int_0^\pi f(t) \, dt = \frac{1}{\pi^3} \int_0^\pi t^2 \sin(t) \, dt = \frac{\pi^2 + 4}{\pi^3}.
$$

</details>
:::

::: exercise-box
**Énoncé 8**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$n \sqrt{\left(1 + \left(\frac{1}{n}\right)^2\right)\left(1 + \left(\frac{2}{n}\right)^2\right) \cdots \left(1 + \left(\frac{n}{n}\right)^2\right)}$$

<details>

<summary><strong>Corrigé</strong></summary>

<!-- Insère la solution ici -->

On pose $$
g_n = n \sqrt{\left(1 + \left(\frac{1}{n}\right)^2\right)\left(1 + \left(\frac{2}{n}\right)^2\right) \cdots \left(1 + \left(\frac{n}{n}\right)^2\right)}
$$

Indication:

On pose $$
G_n = \ln(g_n) = \frac{1}{n} \sum_{k=1}^{n} \ln\left(1 + \frac{k}{n}\right)
$$

Avec $f(t) = \ln(1+t)$ sur $[0,1]$, on reconnaît la somme de Riemann et la subdivision régulière est $$
\sigma_{n}^{k} = \frac{k}{n}, \quad k \in \{1, \dots, n\}.
$$ Comme $f$ est continue sur $[0,1]$, donc elle est intégrable au sens de Riemann sur $[0,1]$, et $$
\int_0^1 \ln(1+t) \, dt = 2\ln(2) - 1.
$$

Or grâce à la continuité de la fonction $\ln$, on a : $$
\lim_{n \to +\infty} g_n = e^{2\ln(2) - 1} = \frac{4}{e}.
$$

</details>
:::

::: exercise-box
**Énoncé 9**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\left( \frac{n+1}{\sqrt{n}} \cdot \frac{n+2}{\sqrt{2n}} \cdots \frac{2n}{\sqrt{n^2}} \right)^{\frac{1}{\ln(n)}}$$

<details>

<summary><strong>Corrigé</strong></summary>

<!-- Insère la solution ici -->

Indication:

On applique $\ln(x_n)$

</details>
:::

::: exercise-box
**Énoncé 10**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\sum_{k=1}^{n} \tan^2\left(\frac{1}{\sqrt{n+k}}\right)$$

<details>

<summary><strong>Corrigé</strong></summary>

<!-- Insère la solution ici -->

La limite de cette suite est ...

</details>
:::

::: exercise-box
**Énoncé 11**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\frac{1}{n} \sum_{k=0}^{n-1} (n - k) \int_{\frac{k}{n}}^{\frac{k+1}{n}} f(t) \, dt,$$ où $f$ est une fonction continue sur $[0, 1]$

<details>

<summary><strong>Corrigé</strong></summary>

<!-- Insère la solution ici -->

La limite de cette suite est ...

</details>
:::

::: exercise-box
**Énoncé 12**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\sum_{n=1}^{n} \sin\left(\frac{k}{n}\right) \sin\left(\frac{k}{n^2}\right)$$ (utiliser un encadrement de $\sin(x)$)

<details>

<summary><strong>Corrigé</strong></summary>

<!-- Insère la solution ici -->

La limite de cette suite est ...

</details>
:::

::: exercise-box
**Énoncé 13**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\ln\left(1 + \frac{\pi}{n}\right) \sum_{k=0}^{n-1} \frac{1}{2 + \cos\left(\frac{3k \pi}{n}\right)}$$

<details>

<summary><strong>Corrigé</strong></summary>

<!-- Insère la solution ici -->

Indication:

On donne une équivalence de $\ln\left(1 + \frac{\pi}{n}\right)$.

Puis sur l'intégrale, après avoir reconnu la fonction associée,

on effectue un changement de variable: $u = \tan\left(\frac{x}{2}\right)$

</details>
:::

::: exercise-box
**Énoncé 14**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\frac{\sqrt{n!}}{n^n}$$

<details>

<summary><strong>Corrigé</strong></summary>

<!-- Insère la solution ici -->

Pareil,

On pose $V_n = \ln(u_n)$, avec $u_n = \frac{\sqrt{n!}}{n^n}$ et par la continuité de $\ln$, on arrive à trouver le résultat voulu.

</details>
:::

::: exercise-box
**Énoncé 15**

Calculer la limite de la suite suivante quand $n \to \infty$ :

$$\frac{1}{n+2}+\frac{1}{n+2}+ \cdots +\frac{1}{kn}$$

<details>

<summary><strong>Corrigé</strong></summary>

Indication: On factorise par $\frac{1}{n}$,

Puis on reconnaît la fonction $f(t) = \frac{1}{1+t}$ sur l'intervalle $[0,k-1]$. Et enfin, on obtient le résultat voulu.

</details>
:::

::: exercise-box
**Exercice 16**

Calculer la limite de la suite suivante :

$$ u_n = \sum_{k=0}^{n-1} \frac{1}{k^2 + n^2} $$

<details>

<summary>Correction</summary>

1.  Soit $u_n = \sum_{k=0}^{n-1} \frac{1}{k^2 + n^2} = \frac{1}{n} \sum_{k=0}^{n-1} \frac{1}{\left(\frac{k}{n}\right)^2 + 1}$. En posant $f(x) = \frac{1}{1 + x^2}$, nous venons d'écrire la somme de Riemann correspondant à $\int_0^1 f(x) \, dx$. Cette intégrale se calcule facilement :

$$
\int_0^1 \frac{dt}{1 + t^2} = \left[ \arctan(t) \right]_0^1 = \frac{\pi}{4} - 0 = \frac{\pi}{4}.
$$

La somme de Riemann $u_n$, convergeant vers $\int_0^1 f(x) \, dx$, nous venons de montrer que $u_n$ converge vers $\frac{\pi}{4}$.

</details>
:::

::: exercise-box
**Exercice 17**

Calculer la limite de la suite suivante :

$$ v_n = \prod_{k=1}^{n} \left(1 + \frac{k^2}{n^2} \right)^{\frac{1}{n}} $$

<details>

<summary>Correction</summary>

2.  Soit $v_n = \prod_{k=1}^{n} \left(1 + \frac{k^2}{n^2} \right)^{\frac{1}{n}}$. Notons

$$
w_n = \ln(v_n) = \frac{1}{n} \sum_{k=1}^{n} \ln\left(1 + \frac{k^2}{n^2} \right).
$$

En posant $g(x) = \ln(1 + x^2)$, nous reconnaissons la somme de Riemann correspondant à $\int_0^1 g(x) \, dx$. Calculons cette intégrale :

$$
I = \int_0^1 g(x) \, dx = \int_0^1 \ln(1 + x^2) \, dx.
$$

Utilisons l'intégration par parties :

$$
\begin{aligned}
I &= \left[ x \ln(1 + x^2) \right]_{0}^{1} - \int_{0}^{1} \frac{2x}{1 + x^2} x \, dx \\
  &= \ln(1 + 1^2) - 2 \int_{0}^{1} \frac{x^2}{1 + x^2} \, dx \\
  &= \ln(2) - 2 \left( \int_{0}^{1} 1 - \frac{1}{1 + x^2} \, dx \right) \\
  &= \ln(2) - 2 \left( \left[ x \right]_{0}^{1} - \int_{0}^{1} \frac{dx}{1 + x^2} \right) \\
  &= \ln(2) - 2 \left( 1 - \frac{\pi}{4} \right) \\
  &= \ln(2) - 2 + \frac{\pi}{2}.
\end{aligned}
$$

Nous venons de prouver que $w_n = \ln(v_n)$ converge vers $I = \ln(2) - 2 + \frac{\pi}{2}$, et puisque la fonction $\exp$ est continue, alors $v_n = \exp(w_n)$ converge vers

$$
\exp \left( \ln(2) - 2 + \frac{\pi}{2} \right) = 2 \exp \left( \frac{\pi}{2} - 2 \right).
$$

Conclusion : $(v_n)$ a pour limite $2\exp\left( \frac{\pi}{2} - 2 \right)$.

</details>
:::
