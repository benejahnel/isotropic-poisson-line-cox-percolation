# 04 — Plan step 1: Lemma D for high levels. Result: not achieved; a sharper reduction and a new obstruction

Conventions as in `02`: $r=1$, $N(z)$ = number of lines meeting $Q(z)$, $R(\gamma)=\sum_{z\in\gamma}N(z)$, target $h_1^*<\infty$ a.s.

## 1. Correction to the exponent table of `02`

The density of *distinct* $m$-bundles of length $\approx t$ (all $m$ lines within a strip of width $O(1)$ over length $t$) is
$$\rho_m(t)\asymp\mu^m\,t^{-m}\qquad(\text{not }\mu^mt^{1-m}/m!),$$
because the strip-counting in `02` counted each bundle once per unit position along its length. Check for $m=2$: intersection points have intensity $\asymp\mu^2$ and the angle $\alpha$ at a typical intersection has density $\propto\sin\alpha$, so pairs of size $\ge t$ (angle $\le C/t$) have density $\asymp\mu^2t^{-2}$. Consequences: size/spacing of $m$-bundles $\asymp\mu^{m/2}t^{1-m/2}$, bounded for $m=2$, decaying for $m\ge3$; Martin's integrability condition $\int P(W>w)^{1/2}dw<\infty$ holds for $m\ge3$ and fails logarithmically for $m=2$ — harmless since the level-2 contribution is trivially $\le1$ per site. The qualitative conclusions of `02` are unchanged.

## 2. An exact "sandwich" identity (rigorous)

For a box $z$ with $N(z)\ge3$, order the lines through $Q(z)$ by their angle in $[0,\pi)$. Call $\ell$ **sandwiched at $z$** if $\ell$ meets $Q(z)$ and is neither the smallest nor the largest angle among the lines through $Q(z)$. Let $Z(\ell)=\{z:\ell\text{ sandwiched at }z\}\subseteq\operatorname{strip}(\ell)$. Then for every box $z$, $(N(z)-2)^+=\#\{\ell:\ell\text{ sandwiched at }z\}$, hence for every path $\gamma$
$$R(\gamma)=\sum_{z\in\gamma}N(z)\le2\,\#\gamma+\sum_{\ell\in\mathcal L}\#\bigl(\gamma\cap Z(\ell)\bigr).\qquad(\dagger)$$
This replaces the level-set/cluster bookkeeping of `02` and the triple-counting attempted here: **no symmetric enumeration over $m$-subsets is needed**, and thick bundles are counted exactly (a $j$-bundle of length $t$ contributes $(j-2)t$ to the right-hand side, not $\binom j3t$). The same identity with "neither among the two smallest nor the largest" gives $(N-3)^+$, etc., so "plan step 1 ($m\ge4$)" is the statement for $Z_2(\ell)$ = boxes where $\ell$ has at least two lines on one angular side and one on the other.

Structure of $Z(\ell)$: a line $\ell'$ at angle $\beta$ to $\ell$ is within distance $2$ of $\ell$ on an interval of length $4/\sin\beta$ (its *partner interval*). Given $\ell$, the partner intervals form a Poisson process along $\ell$; intervals of length $\in[s,2s]$ start at rate $\asymp\mu/s^2$ per unit length (crossing rate $\propto\mu\beta\,d\beta$ at angle $\beta\approx4/s$). $Z(\ell)$ is the set of points of $\ell$ covered by partner intervals on *both* angular sides. Expected coverage density is $O(\mu)$, dominated by short intervals; $E(\text{interval length})<\infty$, $E(\text{length}^2)=\infty$ (log).

## 3. The dyadic (CGGK-type) scheme and where it breaks

Decompose $Z(\ell)$ into maximal runs; a run of length $\in[2^k,2^{k+1})$ is of class $k$, $t=2^k$. A path $\gamma$ of length $n$ gains at most $2t$ from each class-$k$ run it touches. Coarse-grain to boxes of side $\ell_k$ with $\rho_k\ell_k^2=1$, where $\rho_k\asymp\mu^3t^{-3}$ is the bulk density of class-$k$ runs (dominant witness: a 3-bundle of length $\approx t$ with $\ell$ in the middle). Then $\gamma$ touches $\le49(8n/\ell_k+5)$ such boxes and
$$\text{gain}_k\le2t\cdot K\cdot49(8n/\ell_k+5)\quad\Longrightarrow\quad\sum_k\text{gain}_k\le CK\mu^{3/2}n\sum_k2^{-k/2}+o(n),$$
**provided** that a.s. for large $n$ every connected set $A$ of $m$ boxes of side $\ell_k$ in $[-3n,3n]^2$ satisfies $M_k(A)\le Km$, where $M_k(A)$ is the number of class-$k$ runs with left endpoint in $\bigcup A$. (For large $\mu$ the same scheme works with $\mu$-dependent constants: runs shorter than $T_0(\mu)\approx e^{c\mu}$ have density $\mu/T_0$ and contribute a finite constant.)

The union bound over the $\le c^m$ connected sets needs $P(M_k(A)\ge Km)\le e^{-c'm}$ with $c'>\log c$. **This fails.** Take $A$ a row of $m$ boxes (a thin region of length $m\ell_k$). With probability $\asymp\mu^2\ell_k/m^2$ (polynomial in $m$) there is a 2-bundle $(\ell,\ell')$ running along the whole row. Given such a "highway", the class-$k$ runs of $\ell$ are produced by third lines with partner intervals of length $\approx t$ on the other side, which occur at rate $\asymp\mu/t$ per unit length; so $M_k(A)\asymp\mu m\ell_k/t\asymp m\sqrt{t/\mu}\gg Km$ with probability $\gtrsim\mu^2\ell_k/m^2$. Hence
$$P(M_k(A)\ge Km)\ge c\,\mu^2\ell_k\,m^{-2},$$
not exponentially small, and the union bound is lost. (Thick bundles and crowding, the two failure modes identified in `02`/`03`, are *not* the problem here: thanks to $(\dagger)$ a thick bundle of $j$ lines costs $(\mu/t)^j$ for $j-2$ runs, and crowding costs $e^{-L\log L}$ for $L$ lines, both fine.)

The greedy gain itself is not large on a highway: the third lines cover only a fraction $O(\mu)$ of the highway, so the gain rate along it is $O(\mu)$. The scheme fails only because it bounds "gain $\le2t\times$(number of runs)" while on a highway the runs are dense but each is worth exactly its length. In other words, class-$k$ runs are **not** spread with density $\rho_k$: they cluster along 2-bundles, those along 3-bundles, etc. The level-set clusters of `02` have a hierarchical structure, and any proof must respect it.

## 4. Consequence for the plan

* Step 1 of the plan (high levels $m\ge4$ first) does **not** avoid the obstruction: for $Z_2(\ell)$ the highways are 3-bundles (probability $\asymp\mu^3\ell_k/m^3$, still polynomial) and the argument fails identically.
* What a proof needs is an induction over bundle levels $j=1,2,3,\dots$: a $j$-bundle of length $T$ is a highway along which $(j+1)$-sub-bundles of length $s$ occur at rate $\asymp\mu/s^2$ per unit length (so the expected number of sub-bundles of length $\ge T/2$ is $O(\mu/T)$ and the expected sub-bundle *coverage* is $O(\mu)$). The gain of a path is $\sum_j(\text{time spent on }j\text{-bundles})\times(j-2)^+$, and the induction must show that the time a path of length $n$ can spend on $j$-bundles is $\le\varepsilon_jn$ with $\sum_j(j-2)\varepsilon_j<\infty$. The $j=2$ level is where Martin's condition is borderline, which is exactly why the highway probability is only polynomial.
* I could not carry out this induction in the session. The $j=2$ base case alone requires a greedy bound for a Poisson process of segments (the 2-bundles) with length tail $t^{-2}$, i.e. the borderline case of Martin (2002), **plus** the fact that a path gains nothing from a 2-bundle itself (level-2 contribution $\le1$) — the segments only act as carriers of the next level. A clean formulation of this "carrier" structure is the missing idea.

## 5. Verdict on plan step 1 (stop rule)

Not achieved. The session produced: the correction in §1, the exact identity $(\dagger)$ (which removes the Bell-number bookkeeping that was the declared obstacle in `02`/`03`), the explicit computation showing that the dyadic union-bound scheme fails for a *new* reason (polynomially likely highways), and the identification of the required hierarchical induction. Per the stop rule, I recommend not continuing with the same approach; the next attempt should start from the hierarchical induction of §4, and I would estimate it as a multi-week project rather than a session.
