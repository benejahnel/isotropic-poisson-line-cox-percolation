# Analysis of the subcritical phase — summary (2 November 2026, updated after plan step 1)

Files: `01-review.md` (adversarial review of the note's proofs), `02-greedy-conjecture.md` (Conjecture 7.2), `03-sparse-regime.md` (sparse regime $\mu r\le m_0$).

**Verdict.** $\lambda_c(\mu,r)>0$ remains unproved, in general and in the sparse regime. Progress:

1. All rigorous statements of the working note are correct (three presentation fixes).
2. Conjecture 7.2 is implied by the linear statement $h_1^*<\infty$ (reward $\sum N$ instead of $\sum\log N$), which reduces to a greedy chain bound over the clusters of the level sets $\{N\ge m\}$, $m\ge3$ (Lemma D in `02`). Heuristic exponents: clusters of $m$-bundles of length $t$ have density $\asymp\mu^mt^{1-m}/m!$, so the gain rate is $\lesssim\mu^{m/2}/\sqrt{m!}$, summable in $m$.
3. In the sparse regime, the two probabilistic inputs are proved (`03`, Lemmas A and B): crossing a stretch of $j$ lines of length $t$ costs $(4e\sqrt2\lambda j)^{(t-6)/2}$; thick bundles ($\ge j_0\asymp1/\lambda$ lines over length $t$) have probability $\le(C\mu/t)^{j_0}$. Entropy of arrangement paths is $O(\mu)$ per unit length, so the balance entropy/cost works for small $\lambda$ at every $\mu$.
4. Rigorously excluded: all path-level first-moment arguments, including counting bad paths (expected number of bad micro-paths inside a bundle is $\ge2^{n/2}(\mu/n)^H$).

**The single missing ingredient**, common to both routes, is a deterministic decomposition/enumeration of bundles (Lemma C in `03`, item (i) under Lemma D in `02`) that avoids re-counting the same lines (Bell-number factors). It is bookkeeping, but it is the whole difficulty; I did not complete it.

---

**Update (plan step 1, file `04-plan-step1.md`).** Not achieved; stop rule applied. New: (i) corrected bundle densities $\rho_m(t)\asymp\mu^mt^{-m}$; (ii) an exact identity $R(\gamma)\le2\#\gamma+\sum_\ell\#(\gamma\cap Z(\ell))$ with $Z(\ell)$ the boxes where $\ell$ is angularly sandwiched — this removes the Bell-number bookkeeping entirely; (iii) the dyadic CGGK-type union bound then fails for a different reason: 2-bundle "highways" of length $m\ell_k$ have polynomial probability $\asymp\mu^2\ell_k/m^2$ and carry $\asymp m\sqrt{t/\mu}$ class-$k$ runs, so no exponential tail over connected regions is available. The true gain along a highway is only $O(\mu)$ per unit length, so the conjecture is unaffected, but the proof must be a hierarchical induction over bundle levels. Recommendation: treat as a multi-week project; do not continue by sessions of the present kind.
