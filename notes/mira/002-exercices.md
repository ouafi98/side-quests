# Exercises

## Chapter 2B

::::{admonition} Exercise 2B.3
:class: tip

Suppose $\mathcal S$ is the smallest $\sigma-algebra$ on $\mathbb R$ containing
$\{(r,s] : r,s \in \mathbb Q\}$.
Prove that $\mathcal S$ is the collection of Borel subsets of $\mathbb R$.

:::{dropdown} Solution

We prove that $\mathcal S = \mathcal B(\mathbb R)$, where $\mathcal B(\mathbb R)$ is the
smallest $\sigma-algebra$ on $\mathbb R$ containing all open subsets of $\mathbb R$ and it is called
the collection of Borel subsets of $\mathbb R$.

---

**Step 1.** $\mathcal S \subset \mathcal B(\mathbb R)$.

Fix $r,s \in \mathbb Q$. Observe that

$$
(r,s] = \bigcap_{k=1}^{\infty} (r, s + 1/k).
$$

Each interval $(r, s + 1/k)$ is open, hence belongs to $\mathcal B(\mathbb R)$.
Because $\mathcal B(\mathbb R)$ is a $\sigma-algebra$, it follows that
$(r,s] \in \mathcal B(\mathbb R)$.
Since $\mathcal S$ is the smallest $\sigma-algebra$ containing all such intervals,
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

$\blacksquare$

:::
::::

::::{admonition} Exercise 2B.4
:class: tip

Suppose $\mathcal S$ is the smallest $\sigma$-algebra on $\mathbb R$ containing
$\{(r,n] : r \in \mathbb Q,\ n \in \mathbb Z\}$.
Prove that $\mathcal S$ is the collection of Borel subsets of $\mathbb R$.

:::{dropdown} Solution

We prove that $\mathcal S = \mathcal B(\mathbb R)$.

---

**Step 1.** $\mathcal S \subset \mathcal B(\mathbb R)$.

Fix $r \in \mathbb Q$ and $n \in \mathbb Z$. Observe that

$$
(r,n] = \bigcap_{k=1}^{\infty} (r, n + 1/k).
$$

Each interval $(r,n+1/k)$ is open, hence belongs to $\mathcal B(\mathbb R)$.
Because $\mathcal B(\mathbb R)$ is a $\sigma$-algebra, it follows that
$(r,n] \in \mathcal B(\mathbb R)$.
Since $\mathcal S$ is the smallest $\sigma$-algebra containing all such intervals,
we conclude that

$$
\mathcal S \subset \mathcal B(\mathbb R).
$$

---

**Step 2.** Construction of half-lines.

We first consider the case $a > 0$.
Using the sequences $s_n(a) \downarrow a$, we can write

$$
(a,+\infty)
=
\bigcup_{k=1}^{\infty}
\ \bigcup_{n=1}^{\infty}
(\, s_n(a), \, k \,].
$$

Each interval $(s_n(a),k]$ is of the form $(r,n]$ with rational and integer endpoints,
hence belongs to $\mathcal S$. The remaining case $a < 0$ is shown using a similar argument. (see exercice 2B.3)

Therefore $(a,+\infty) \in \mathcal S, \, \forall a \in \mathbb R$

Next, observe that

$$
[a,+\infty)
=
\bigcap_{k=1}^{\infty} (a - 1/k,+\infty).
$$

Since $\mathcal S$ is a $\sigma$-algebra, it follows that $[a,+\infty) \in \mathcal S$.
Taking complements, we obtain

$$
(-\infty,a) = \mathbb R \setminus [a,+\infty) \in \mathcal S.
$$

---

**Step 3.** Construction of open intervals.

Let $a < b$. Then

$$
(a,b) = (-\infty,b) \cap (a,+\infty).
$$

Since both $(-\infty,b)$ and $(a,+\infty)$ belong to $\mathcal S$, we conclude that
$(a,b) \in \mathcal S$.

Thus every open interval of $\mathbb R$ belongs to $\mathcal S$.

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

$\blacksquare$

:::
::::

::::{admonition} Exercise 2B.7
:class: tip

Prove that the collection of Borel subsets of $\mathbb R$ is translation invariant.
More precisely, prove that if $B \subset \mathbb R$ is a Borel set and $t \in \mathbb R$,
then $t + B$ is a Borel subset of $\mathbb R$.

:::{dropdown} Solution

Let $B \subset \mathbb R$ be a Borel set and let $t \in \mathbb R$.
Define the function $f : \mathbb R \to \mathbb R$ by

$$
f(x) = x - t.
$$

The function $f$ is continuous on $\mathbb R$, hence it is Borel measurable.
Therefore, for every Borel set $B \subset \mathbb R$, the inverse image $f^{-1}(B)$
is a Borel subset of $\mathbb R$.

Now observe that

$$
f^{-1}(B)
=
\{ x \in \mathbb R : f(x) \in B \}
=
\{ x \in \mathbb R : x - t \in B \}
=
t + B.
$$

Hence $t + B$ is a Borel subset of $\mathbb R$.

$\blacksquare$

:::
::::

::::{admonition} Exercise 2B.9
:class: tip

Give an example of a measurable space $(X,\mathcal S)$ and a function
$f : X \to \mathbb R$ such that $|f|$ is $\mathcal S$-measurable but
$f$ is not $\mathcal S$-measurable.

:::{dropdown} Solution

Define
$\mathcal S = \{ A \cup B : A \subseteq [0,+\infty),\ B \in \{\varnothing,(-\infty,0)\} \}.$

---

**Step 1. $\mathcal S$ is a $\sigma$-algebra on $\mathbb R$**

- $\varnothing = \varnothing \cup \varnothing \in \mathcal S$, and

  $$
  \mathbb R = (-\infty,0) \cup [0,+\infty) \in \mathcal S.
  $$

- Let $C \in \mathcal S$ with $C = A \cup B$, where
  $A \subseteq [0,+\infty)$ and $B \in \{\varnothing,(-\infty,0)\}$.
  Then

  $$
  \mathbb R \setminus C = (\mathbb R \setminus A) \cap (\mathbb R \setminus B).
  $$

  Since

  $$
  \mathbb R \setminus A
  =
  (-\infty,0) \cup ([0,+\infty)\setminus A),
  $$

  and

  $$
  \mathbb R \setminus B =
  \begin{cases}
  \mathbb R & \text{if } B=\varnothing,\\
  [0,+\infty) & \text{if } B=(-\infty,0),
  \end{cases}
  $$

  it follows that $\mathbb R \setminus C$ is again of the form $A' \cup B'$ with
  $A' \subseteq [0,+\infty)$ and
  $B' \in \{\varnothing,(-\infty,0)\}$.
  Hence $\mathbb R \setminus C \in \mathcal S$.

- Let $(C_k)_{k\ge1}$ be a sequence of elements of $\mathcal S$ with
  $C_k = A_k \cup B_k$.
  Then

  $$
  \bigcup_{k=1}^\infty C_k
  =
  \left( \bigcup_{k=1}^\infty A_k \right)
  \cup
  \left( \bigcup_{k=1}^\infty B_k \right).
  $$

  Since $A_k \subseteq [0,+\infty)$ for all $k$ and
  $\bigcup_k B_k \in \{\varnothing,(-\infty,0)\}$,
  we have $\bigcup_k C_k \in \mathcal S$.

Therefore, $\mathcal S$ is a $\sigma$-algebra on $\mathbb R$.

---

**Step 2. Definition of the function.**

Define $f : \mathbb R \to \mathbb R$ by
$$
f(x)=
\begin{cases}
-1 & \text{if } x \le -1,\\
1 & \text{if } x > -1.
\end{cases}
$$

---

**Step 3. $f$ is not $\mathcal S$-measurable.**

Consider the Borel set $\{1\} \subset \mathbb R$. Then

$$
f^{-1}(\{1\}) = (-1,+\infty).
$$

This set contains some negative values but not all of $(-\infty,0)$.
By definition of $\mathcal S$, such a set does not belong to $\mathcal S$.
Hence $f$ is not $\mathcal S$-measurable.

---

**Step 4. $|f|$ is $\mathcal S$-measurable.**

For all $x \in \mathbb R$, $|f(x)| = 1$.
Thus $|f|$ is constant, and therefore $\mathcal S$-measurable.

---

Hence $|f|$ is $\mathcal S$-measurable but $f$ is not.

$\blacksquare$

:::
::::

::::{admonition} Exercise 2B.16
:class: tip

Suppose $(X,\mathcal S)$ is a measurable space and $A \in \mathcal S$.

Define
$$ \mathcal S_A = \{ E \in \mathcal S : A \subset E \text{ or } A \cap E = \varnothing \}. $$

(a) Prove that $\mathcal S_A$ is a $\sigma$-algebra on $X$.

(b) Prove that a function $f : X \to \mathbb R$ is $\mathcal S_A$-measurable
if and only if $f$ is $\mathcal S$-measurable and $f$ is constant on $A$.

:::{dropdown} Solution

(a)  $\mathcal S_A$ is a $\sigma$-algebra.

**Step 1.** $\varnothing, X \in \mathcal S_A$.

- Since $A \cap \varnothing = \varnothing$, we have $\varnothing \in \mathcal S_A$.
- Since $A \subset X$, we have $X \in \mathcal S_A$.

---

**Step 2.** Closed under complements.

Let $E \in \mathcal S_A$.

Then either $A \subset E$ or $A \cap E = \varnothing$.

- If $A \subset E$, then $A \cap (X \setminus E) = \varnothing$,
  hence $X \setminus E \in \mathcal S_A$.

- If $A \cap E = \varnothing$, then $A \subset X \setminus E$,
  hence $X \setminus E \in \mathcal S_A$.

Thus $\mathcal S_A$ is closed under complements.

---

**Step 3.** Closed under countable unions.

Let $(E_k)_{k\ge1}$ be a sequence of elements of $\mathcal S_A$.

We consider two cases.

- If there exists $k$ such that $A \subset E_k$, then
  $A \subset \bigcup_{k=1}^\infty E_k$,
  so the union belongs to $\mathcal S_A$.

- Otherwise, for every $k$ we have $A \cap E_k = \varnothing$.
  Then
  $$ A \cap \left( \bigcup_{k=1}^\infty E_k \right) = \bigcup_{k=1}^\infty (A \cap E_k) = \varnothing, $$
  so the union belongs to $\mathcal S_A$.

Therefore $\mathcal S_A$ is a $\sigma$-algebra on $X$.

---

(b) Characterization of $\mathcal S_A$-measurable functions

---

($\Rightarrow$) Assume $f$ is $\mathcal S_A$-measurable.

Since $\mathcal S_A \subset \mathcal S$, we have
$f^{-1}((a,+\infty)) \in \mathcal S$ for every $a \in \mathbb R$.
Hence $f$ is $\mathcal S$-measurable.

Now suppose $f$ is not constant on $A$.
Then there exist $a_1, a_2 \in A$ such that
$$
f(a_1) \ne f(a_2).
$$

Consider the Borel set $\{ f(a_1) \}$.
Since $f$ is $\mathcal S_A$-measurable,
$$
f^{-1}(\{f(a_1)\}) \in \mathcal S_A.
$$

By definition of $\mathcal S_A$, either

- $A \subset f^{-1}(\{f(a_1)\})$, or
- $A \cap f^{-1}(\{f(a_1)\}) = \varnothing$.

The second possibility is impossible because $a_1 \in A$
and $f(a_1)$ belongs to that singleton.

Hence
$$
A \subset f^{-1}(\{f(a_1)\}).
$$

This implies that for every $x \in A$,
$$
f(x) = f(a_1).
$$

In particular,
$$
f(a_2) = f(a_1),
$$
which contradicts the assumption that
$f(a_1) \ne f(a_2)$.

Therefore $f$ must be constant on $A$.

---

($\Leftarrow$) Assume $f$ is $\mathcal S$-measurable and constant on $A$.

Let $f(x)=c$ for all $x \in A$.

To prove $f$ is $\mathcal S_A$-measurable,
it suffices to check that
$$
f^{-1}((a,+\infty)) \in \mathcal S_A
\quad \text{for all } a \in \mathbb R.
$$

We distinguish two cases.

- If $c < a$, then
  $A \cap f^{-1}((a,+\infty)) = \varnothing$.
  Since $f^{-1}((a,+\infty)) \in \mathcal S$,
  it follows that it belongs to $\mathcal S_A$.

- If $a \le c$, then
  $A \subset f^{-1}((a,+\infty))$.
  Since the set lies in $\mathcal S$,
  it belongs to $\mathcal S_A$.

Thus $f$ is $\mathcal S_A$-measurable.

---

Therefore, $f$ is $\mathcal S_A$-measurable
if and only if $f$ is $\mathcal S$-measurable
and $f$ is constant on $A$.

$\blacksquare$

:::
::::

::::{admonition} Exercise 2B.17
:class: tip

Suppose $X$ is a Borel subset of $\mathbb R$ and $f : X \to \mathbb R$ is a function such that
$$
\{x \in X : f \text{ is not continuous at } x\}
$$
is a countable set. Prove $f$ is a Borel measurable function.

:::{dropdown} Solution

Let
$$
A = \{x \in X : f \text{ is not continuous at } x\}.
$$
By hypothesis, $A$ is countable.

To prove that $f$ is Borel measurable, it suffices to show that
for every $a \in \mathbb R$,
$$
f^{-1}((a,+\infty))
$$
is a Borel set.

Fix $a \in \mathbb R$.

We decompose
$$ f^{-1}((a,+\infty)) = \big(f^{-1}((a,+\infty)) \setminus A\big) \cup \big(f^{-1}((a,+\infty)) \cap A\big). $$

---

**Step 1. The part outside the discontinuities**

Let
$$
E = f^{-1}((a,+\infty)) \setminus A.
$$

If $x \in E$, then $x$ is a point of continuity of $f$
and $f(x) > a$.

By continuity at $x$, there exists $\delta_x > 0$ such that
for all
$$
y \in (x-\delta_x, x+\delta_x) \cap X,
$$
we have
$$
f(y) > a.
$$

Hence
$$
(x-\delta_x, x+\delta_x) \cap X
\subset
E.
$$

Therefore,
$$
E=\left(\bigcup_{x \in E} (x-\delta_x, x+\delta_x) \right) \cap X.
$$

The union of open intervals is an open subset of $\mathbb R$.
Since $X$ is Borel, the intersection of an open set with $X$
is Borel.

Thus $E$ is a Borel set.

**Step 2. The part inside the discontinuities**

Now consider
$$
f^{-1}((a,+\infty)) \cap A.
$$

Since this set is contained in $A$ and $A$ is countable,
it is countable.
Every countable subset of $\mathbb R$ is Borel.

Hence this set is Borel.

---

**Step 3. Conclusion**

We have written
$$
f^{-1}((a,+\infty)) = E \cup \big(f^{-1}((a,+\infty)) \cap A\big),
$$
as a union of two Borel sets.

Therefore
$f^{-1}((a,+\infty))$ is Borel.

Since this holds for every $a \in \mathbb R$,
$f$ is Borel measurable.

$\blacksquare$

:::
::::

::::{admonition} Exercise 2B.18
:class: tip

Suppose $f : \mathbb R \to \mathbb R$ is differentiable at every element of $\mathbb R$. Prove the $f'$ is 
a Borel measurable function from $\mathbb R$ to $\mathbb R$.

:::{dropdown} Solution
in progess :)
:::
::::