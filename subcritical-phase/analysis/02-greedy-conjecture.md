# 02 — Conjecture 7.2 (linear greedy growth): reformulations, obstructions, and a reduction

Notation as in the note: $r=1$ w.l.o.g., $Q(z)=z+[0,1]^2$, $N(z)=\#\{\ell\in\mathcal L:\ell\cap Q(z)\neq\emptyset\}$, $\Gamma_n(z_0)$ the self-avoiding $2$-paths of length $n$, and
$$h^*=\limsup_n\frac1n\max_{\|z_0\|_\infty\le n}\max_{\gamma\in\Gamma_n(z_0)}\sum_{z\in\gamma}\log N(z).$$

Status: **not proved.** What follows: (A) a linear reformulation that is rigorous and slightly stronger; (B) a precise explanation of why *every* path-level first moment fails, including the "count of bad paths" version; (C) a reduction of the conjecture to a cluster-level greedy statement (Lemma D), with the exponents computed, which I believe is the right rigorous target.

## A. Linear reward (rigorous)

Since $\log N\le N$ (for $N\ge1$; and $\log N=-\infty$ only helps), $h^*\le h_1^*$ where
$$h_1^*:=\limsup_n\frac1n\max_{\|z_0\|_\infty\le n}\max_{\gamma\in\Gamma_n(z_0)}R(\gamma),\qquad R(\gamma):=\sum_{z\in\gamma}N(z)=\sum_{\ell\in\mathcal L}\#\bigl(\gamma\cap\operatorname{strip}(\ell)\bigr),$$
with $\operatorname{strip}(\ell)=\{z:\ell\cap Q(z)\neq\emptyset\}$. So **Conjecture 7.2 follows from $h_1^*<\infty$ a.s.**, and by Thm 5.1/Cor 5.2 this gives $\lambda_c\ge e^{-\log24-h_1^*}/\sqrt2$. The reward is now *linear in the line process*: $R(\gamma)=\sum_\ell f_\gamma(\ell)$ with $f_\gamma(\ell)=\#(\gamma\cap\operatorname{strip}(\ell))\le\min\{n+1,\ 3\,\mathcal H^1(\ell\cap\operatorname{hull})+3\}$.

Elementary facts: $\operatorname{strip}(\ell)$ restricted to a window of side $t$ has at most $3t+3$ sites; $N(z)\sim\mathrm{Poi}(4\mu/\pi)$; the lines meeting $\ge t$ sites of a *straight* row of boxes form a Poisson process of mean $\asymp\mu n/t$ (angle $\lesssim1/t$, $n$ positions).

Also note $h_1^*\ge1$ trivially (follow one line: every box it meets has $N\ge1$), and the heuristics below suggest $h_1^*\le2+O(\mu^{3/2})$.

## B. Why path-level first moments fail (rigorous lower bounds)

1. **$\mathbb E\,Y_n$** is superexponential (Prop 6.1 of the note).
2. **Exponential moments of $R(\gamma)$** are infinite for a straight $\gamma$: $\mathbb E e^{sR(\gamma)}=\exp\int(e^{sf_\gamma}-1)\,d\nu_\mu$ and the lines with $f_\gamma\ge t$ have measure $\asymp\mu n/t$, so $\int e^{sf}d\nu\ge\sum_t\mu(n/t^2)e^{st}=\infty$. No Chernoff bound.
3. **Even the expected number of bad paths is exponentially large.** Let $H\ge1$ and $B_n(H)=\#\{\gamma\in\Gamma_n(0):R(\gamma)\ge Hn/2\}$. If $H$ lines run along the row $[0,n]\times[0,1]$ (probability $\ge c(\mu/n)^H/H!$ by Lemma 2.1), then every $2$-path inside rows $0$ and $-1$ that advances by $1$ or $2$ in each step has $R\ge H\cdot\#\gamma$ and there are $\ge2^{n/2}$ of them of length $n/2$. Hence $\mathbb E B_{n}(H)\ge c\,2^{n/2}(\mu/n)^H/H!\to\infty$. So Borel–Cantelli on $\mathbb E B_n$ cannot work for any threshold $H$: the union bound must be taken over *stretches*, not over micro-paths. (This is the same lesson as in `03-sparse-regime.md`.)
4. **Spatial coarse-graining does not help by itself.** Covering $\gamma$ by $K$-boxes gives $R(\gamma)\le\sum_{b}3(\Lambda(b)+N_K(b))$ over visited $K$-boxes, a greedy-animal problem on the $K$-lattice with light-tailed one-point weights, but a bundle of $j$ lines still produces a row of $K$-boxes each of weight $\asymp Kj$, and the union bound over $K$-animals inside that row reproduces item 3 at scale $K$.

## C. Reduction to a cluster-level greedy statement

Write $R(\gamma)=\sum_{m\ge1}\#(\gamma\cap D_m)$ with level sets $D_m=\{z:N(z)\ge m\}$. Then $h_1^*\le\sum_m\varepsilon_m$ provided
$$(\ast)_m\qquad\text{a.s., for all large }n:\quad\max_{\|z_0\|\le n}\max_{\gamma\in\Gamma_n(z_0)}\#(\gamma\cap D_m)\le\varepsilon_mn,\qquad\sum_m\varepsilon_m<\infty.$$
Trivially $\varepsilon_1=\varepsilon_2=1$ works (and $\varepsilon_m\le1$ always), so only $m\ge3$ matters, and by Lemma 7.1 only $m\le\log n$ matters.

### Structure of $D_m$ for $m\ge3$ (heuristic exponents, each line of the table is a routine Mecke computation)

Sites of $D_m$ come in **clusters** of two kinds:

| cluster type | size (sites) | density per unit area | typical spacing $d$ | size/spacing |
|---|---|---|---|---|
| crossing cluster: $m$ lines through a region of diameter $O(1)$ | $O(1)$ | $\asymp(c\mu)^m/m!$ | $(m!/(c\mu)^m)^{1/2}$ | superexp. small |
| $m$-bundle of length $t$ (all $m$ lines within a strip of width $O(1)$ over length $t$) | $\asymp t$ | $\asymp\mu^m t^{1-m}/m!$ (positions $\times$ directions $1/t$ $\times$ $(\mu/t)^m$) | $\asymp(m!\,t^{m-1}/\mu^m)^{1/2}$ | $\asymp\mu^{m/2}t^{(3-m)/2}/\sqrt{m!}$ |

For $m\ge3$ the ratio size/spacing is bounded by $\mu^{m/2}/\sqrt{m!}$ uniformly in $t$, and for $m\ge4$ it tends to $0$ as $t\to\infty$. A path of length $n$ that visits clusters $C_1,\dots,C_k$ in this order gains $\le\sum|C_i|$ and spends $\ge\sum_i\operatorname{dist}(C_i,C_{i+1})$ steps, so its gain rate is at most $\sup$ over chains of $\sum|C_i|/\sum\operatorname{dist}(C_i,C_{i+1})$. The table suggests $\varepsilon_m\asymp\mu^{m/2}/\sqrt{m!}$, which is summable. (For $m=2$ the ratio $\mu\sqrt t$ is unbounded, consistent with $\varepsilon_2=1$: a path can chain $2$-bundles almost without gaps. This is harmless.)

### Lemma D (cluster-chain bound; the proposed rigorous target)

Let $m\ge3$ and let $\mathcal C_m$ be the set of connected components (for $2$-adjacency) of $D_m$. **Claim to prove:** there are $\varepsilon_m$ with $\sum_m\varepsilon_m<\infty$ such that a.s. for all large $n$, every sequence $C_1,\dots,C_k$ of distinct components of $D_m$ inside $[-3n,3n]^2$ satisfies
$$\sum_{i=1}^k|C_i|\le\varepsilon_m\Bigl(n+\sum_{i=1}^{k-1}\operatorname{dist}_\infty(C_i,C_{i+1})\Bigr).$$
Given Lemma D, $(\ast)_m$ follows (a path of length $n$ visits components in some order and its length dominates the sum of the distances), hence $h_1^*\le2+\sum_{m\ge3}\varepsilon_m<\infty$ and **Conjecture 7.2 and $\lambda_c>0$ follow for all $\mu,r$**.

Why Lemma D is more tractable than the path statement: the union bound is now over *sequences of components*, and the number of components of $D_m$ in $[-3n,3n]^2$ is a.s. $O(n^2\mu^m/m!)$ (polynomial, no $24^n$); a component is a rare object whose probability $\asymp\mu^mt^{1-m}/m!$ decays polynomially in its size $t$, which is exactly the regime of the greedy-lattice-animal theory with heavy-tailed but integrable ($\int P(W>w)^{1/2}dw<\infty$ for $m\ge4$, borderline for $m=3$) "cluster weights" — except that the clusters do not form an i.i.d. field and are not points. The dependence is mild in one specific sense that can be exploited: two components at distance $\ge c_kn^{6/k}$ share $<k$ lines (Lemma 7.1 of the note), so for $m\ge2k$ far-apart components are built from disjoint sets of lines and are independent given the remaining lines.

### What I could not do

A complete proof of Lemma D. The obstacle is purely technical: one needs (i) a description of all components of $D_m$ as unions of at most $m$ "bundle segments" with a deterministic enumeration (the Bell-number issue: which $m$ lines form the cluster, and the same set of lines may generate several components), and (ii) the greedy chain argument of Cox–Gandolfi–Griffin–Kesten (1993) / Martin (2002) adapted from i.i.d. site weights to a Poisson process of segments with polynomially decaying size distribution. Step (ii) looks like a known-type argument; step (i) is the same bookkeeping as Lemma C in `03-sparse-regime.md`. I did not find a way around either.

## D. Summary of verdicts

* Conjecture 7.2 is **plausible** and I found no counterexample; the natural guess is $h_1^*=2+O(\mu^{3/2})$ (so $h^*\le\log 2+o(1)$ for small $\mu$).
* It is **equivalent in strength** (for our purpose) to the linear statement $h_1^*<\infty$, which reduces to the cluster-chain Lemma D.
* Every path-level first-moment approach is **rigorously excluded** (Section B), including counting bad paths.
* **Open:** Lemma D. The sparse-regime route (`03`) and the general route (`02`) require the same bookkeeping lemma about bundles; proving it once would settle both.
