# Exercises

## Chapter 2B

::::{admonition} Exercise 2B.3
:class: tip

Suppose $\mathcal S$ is the smallest $\sigma-algebra$ on $\mathbb R$ containing
$\{(r,s] : r,s \in \mathbb Q\}$.
Prove that $\mathcal S$ is the collection of Borel subsets of $\mathbb R$.

:::{dropdown} Solution

We prove that $\mathcal S = \mathcal B(\mathbb R)$, where $\mathcal B(\mathbb R)$ is the
smallest $\sigma$-algebra on $\mathbb R$ containing all open subsets of $\mathbb R$ and it is called
the collection of Borel subsets of $\mathbb R$.

---

**Step 1.** $\mathcal S \subset \mathcal B(\mathbb R)$.

Fix $r,s \in \mathbb Q$. Observe that

$$
(r,s] = \bigcap_{k=1}^{\infty} (r, s + 1/k).
$$

Each interval $(r, s + 1/k)$ is open, hence belongs to $\mathcal B(\mathbb R)$.
Because $\mathcal B(\mathbb R)$ is a $\sigma$-algebra, it follows that
$(r,s] \in \mathcal B(\mathbb R)$.
Since $\mathcal S$ is the smallest $\sigma$-algebra containing all such intervals,
we conclude that

$$
\mathcal S \subset \mathcal B(\mathbb R).
$$

---

**Step 2.** Rational approximation of real numbers.

Let $x \in \mathbb R^+$.
Define $r_n(x)$ as the truncation of $x$ at $n$ digits after the decimal point.
Then:
- $r_n(x) \in \mathbb Q$,
- $r_n(x)$ is increasing,
- $|x - r_n(x)| \le 10^{-n}$.

Define $s_n(x)$ as the truncation of $x$ at $n$ digits after the decimal point,
followed by adding $10^{-n}$. Then:
- $s_n(x) \in \mathbb Q$,
- $s_n(x)$ is decreasing,
- $|x - s_n(x)| \le 10^{-n}$.

Hence $r_n(x) \uparrow x$ and $s_n(x) \downarrow x$.
If $x < 0$, we use $-r_n(-x) \downarrow x$ and $-s_n(-x) \uparrow x$.

---

**Step 3.** Representation of open intervals.

Let $a < b$.

If $a,b > 0$, then

$$
(a,b) = \bigcup_{n=1}^{\infty} (\, s_n(a), \, r_n(b) \,].
$$

If $a < 0 < b$, then

$$
(a,b) = \bigcup_{n=1}^{\infty} (\, -r_n(-a), \, r_n(b) \,].
$$
The case $a,b<0$ follows by the same argument, using the sequences
$-r_n(-x)$ and $-s_n(-x)$.

We now treat an interval with an infinite endpoint.
Let $a \in \mathbb R$.

If $a > 0$, then

$$
(a,+\infty)
=
\bigcup_{m=1}^{\infty}
\ \bigcup_{n=1}^{\infty}
(\, s_n(a), \, m \,].
$$

If $a < 0$, a similar construction using $-r_n(-a)$ yields a representation of
$(a,+\infty)$ as a countable union of intervals $(r,s]$ with rational endpoints.

Similarly, the case $(-\infty,a)$ follow by the same argument, using $r_n(x)$ for $a>0$ and $-s_n(-x)$ for $a<0$.

Thus every open interval of $\mathbb R$ is a countable union of elements of
$\{(r,s] : r,s \in \mathbb Q\}$, and hence belongs to $\mathcal S$.

---

**Step 4.** Conclusion.

Every open subset of $\mathbb R$ is a countable union of open intervals.
Therefore every open set belongs to $\mathcal S$, which implies

$$
\mathcal B(\mathbb R) \subset \mathcal S.
$$

Combining this with Step 1 yields

$$
\mathcal S = \mathcal B(\mathbb R).
$$

∎

:::
::::
