# 01 — Adversarial review of the rigorous statements in `subcritical-phase/main.tex`

Every constant and inequality was recomputed. Verdicts: **correct**, **minor fix**, **gap**, **wrong**.

| Statement | Verdict | Notes |
|---|---|---|
| Lemma 2.1 (lines crossing a strip) | correct | see (1) |
| Prop 3.1 (monotonicity, scaling) | correct | see (2) |
| Lemma 3.2 (mixing) | correct | see (3) |
| Prop 3.3 (quenched 0–1 law, threshold) | correct, minor fix | see (4) |
| Prop 4.1 (quasi-polynomial lower bound) | correct | see (5) |
| Thm 5.1 (quenched path criterion) | correct | see (6) |
| Cor 5.2 (greedy-path criterion) | correct, minor fix | see (7) |
| Prop 6.1 (superexponential annealed moments) | correct | see (8) |
| Lemma 7.1 (shared lines) | correct, minor fix | see (9) |

## (1) Lemma 2.1
Lines through $(0,y_0)$, $y_0\in[a/4,3a/4]$, slope $|b|\le a/(4d)$: height at $x=d$ lies in $[a/4-a/4,\,3a/4+a/4]=[0,a]$. Normal-angle interval has length $2\arctan(a/(4d))$; $\arctan t/t$ is decreasing with value $0.980$ at $t=1/4$, so $\arctan t\ge0.94t$ holds. At fixed $\theta$ the displacement is $s=y_0\sin\theta$ (the set is a product set in $(\theta,s)$ at fixed $\theta$), range of length $(a/2)\sin\theta$, and $\sin\theta=(1+b^2)^{-1/2}\ge(17/16)^{-1/2}=0.970$. Product $0.47\cdot0.485=0.228\ge1/5$. Upper bound: perimeter of a segment of length $a$ is $2a$. Correct.

## (2) Prop 3.1
Superposition/thinning couplings are standard. Scaling: $x\mapsto x/r$ maps $\ell(\theta,s)$ to $\ell(\theta,s/r)$, so the intensity becomes $(\mu r/\pi)\,d\theta\,ds'$; point intensity per unit length becomes $\lambda r$. Correct.

## (3) Lemma 3.2
Let $E=\{$no line in $[W_1]\cap[W_2]\}$, $P(E^c)\le1-e^{-\nu}\le\nu$. Let $F',H'$ be $F,H$ evaluated on the configuration with the shared lines removed; they are independent, and $F=F'$, $H=H'$ on $E$. Then $|P(F\cap H)-P(F')P(H')|\le\nu$ and $|P(F)P(H)-P(F')P(H')|\le2\nu$; total $3\nu$. Shared-line measure: $|x\cdot n_\theta|\le2\rho$ gives angle measure $2\arcsin(2\rho/|x|)\le\pi\cdot2\rho/|x|$ (convexity of $\arcsin$ on $[0,1]$), displacement interval $2\rho$; product $(\mu/\pi)(2\pi\rho/|x|)(2\rho)=4\mu\rho^2/|x|$. The hypothesis $|x|\ge4\rho$ is not even needed. Correct.

## (4) Prop 3.3
- 0–1 law: an unbounded component has infinitely many points (finitely many disks are bounded); an infinite component is unbounded (points locally finite given $\mathcal L$). Removing the finitely many points of a bounded set $B$ from an infinite connected locally finite graph leaves finitely many components (each contains a neighbour of a removed vertex), one of them infinite. So percolation is a tail event for the independent restrictions to annuli. Correct.
- $\lambda_c(\mathcal L)$ is translation invariant for **every** $\mathcal L$ (not only a.s.), so ergodicity (Lemma 3.2) gives a.s. constancy. Correct.
- **Minor fix (presentation):** $\theta_{\mathcal L}(\lambda)$ is a regular conditional probability; one should fix a jointly measurable version in $(\mathcal L,\lambda)$, e.g. define it for rational $\lambda$ and extend by monotonicity. Also state the convention $\sup\emptyset=0$ for $\lambda_c(\mathcal L)$ and allow $c^*=\infty$. No mathematical change.

## (5) Prop 4.1
$a=r/2$, $d=(m+1)r/2$: Lemma 2.1 gives $\nu_m\in[\mu r/(10\pi(m+1)),\,\mu r/\pi]$. Consecutive points in adjacent boxes of side $r/2$ are at distance $\le\sqrt{r^2+r^2/4}=(\sqrt5/2)r<2r$. With $j=\lceil4\log(m+1)/(\lambda r)\rceil$: $e^{-\lambda rj/2}\le(m+1)^{-2}$ and $(1-(m+1)^{-2})^{m+1}\ge1-(m+1)^{-1}\ge1/2$. $P(M\ge j)\ge e^{-\nu_m}\nu_m^j/j!\ge e^{-\mu r/\pi}(\nu_m/j)^j$ with $\nu_m$ replaced by its lower bound (monotone in $\nu$). Logarithm: $-j\log(m+1)-j\log j+O(j)=-(4+o(1))(\log m)^2/(\lambda r)$ since $j\log j=O(\log m\log\log m)$. Correct.

## (6) Thm 5.1
- $\#\Gamma_n\le24^n$: 24 steps of sup-norm $\le2$. Correct.
- $1-e^{-x}\le x$ and $\Lambda(Q^\circ(z))\le\sqrt2\,rN(z)$. Correct.
- $|x-y|<2r$ with $x\in Q^\circ(z)$, $y\in Q^\circ(w)$ forces $|z_i-w_i|\le2$: if $w_1\ge z_1+3$ then $y_1-x_1>r(z_1+3)-r(z_1+1)=2r$. Correct.
- The occupied sites of an infinite component form an infinite 2-connected set (image of a connected graph under a map sending neighbours to equal-or-adjacent sites); the 2-adjacency graph has degree 24, so there are vertices at every graph distance and a shortest path is self-avoiding. Correct.
- Union bound and limit: correct; the case $g^*=+\infty$ gives the trivial bound. The final implication uses Prop 3.3. Correct.
- Remark (not an error): the proof actually gives the stronger quenched bound with weights $\min(1,\lambda\sqrt2 rN(z))$ instead of $\lambda\sqrt2 rN(z)$; this truncation is the natural starting point for attacks on the conjecture (bundles then contribute at most $1$ per site instead of $N$).

## (7) Cor 5.2
$Y_n\le24^n\max_\gamma\prod N$ gives $g^*\le\log24+h^*$. **Minor fix:** the bound $\lambda_c\ge e^{-\log24-\operatorname{ess\,inf}h^*}/(\sqrt2 r)$ needs $h^*$ to be a.s. constant or should be read with $h^*$ replaced by any $h$ with $P(h^*\le h)>0$; $h^*$ is translation invariant (the window $\|z_0\|_\infty\le n$ absorbs any fixed shift asymptotically), hence a.s. constant by ergodicity, so the statement is correct once this is said. Convention $\log0=-\infty$ (empty product $0$) is consistent.

## (8) Prop 6.1
$a=r$, $d=(n+1)r$: $\nu_n\in[\mu r/(5\pi(n+1)),2\mu r/\pi]$. Every line meeting both vertical sides meets each $Q(ke_1)$, so $N(ke_1)\ge M$. $\mathbb E M^{n+1}\ge j^{n+1}P(M\ge j)$. With $j=\lceil n/\log n\rceil$: $(n+1)\log j=n\log n-n\log\log n+o(n)$ and $j\log(\mu r/(5\pi(n+1)j))=-2n+o(n)$. Total $n\log n-O(n\log\log n)$. Correct.

## (9) Lemma 7.1
$\rho=r/\sqrt2$, $D=r\|z-w\|_2$: shared measure $\le4\mu\rho^2/D=2\mu r/\|z-w\|_2$. $P(\mathrm{Poi}(\nu)\ge k)\le\nu^k/k!\le(e\nu/k)^k$. Pairs $\le(2n+1)^4\le81n^4$. With $\|z-w\|_2\ge c_kn^{6/k}$ and $c_k\ge2e\mu r/k$ the per-pair bound is $\le n^{-6}$; total $\le81n^{-2}$, summable. **Minor fix:** for the second claim use $k=\lceil\log n\rceil$ in the Poisson tail (non-integer $k$); the bound $(2n+1)^2(4e\mu r/(\pi\lceil\log n\rceil))^{\lceil\log n\rceil}=n^{-\log\log n+O(1)}$ is summable. Correct.

## Overall
No mathematical error found. Three presentation fixes (measurable version in Prop 3.3; a.s. constancy of $h^*$ in Cor 5.2; integer $k$ in Lemma 7.1). The truncated-weight remark in (6) is recorded for the attack on Conjecture 7.2.
