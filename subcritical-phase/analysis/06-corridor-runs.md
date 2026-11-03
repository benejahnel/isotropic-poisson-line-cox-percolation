# Connected-run counts along a corridor

The complete proof is in `../corridor-runs.tex`, with the rendered note in `../corridor-runs.pdf`. This follow-up answers the proposed upper-tail question for a straight corridor and isolates the dependence that prevents a direct comparison at the mean-density scale.

## What was proved

1. For a stationary one-dimensional Poisson interval union with bounded components, interval start rate rho, and mean coverage multiplicity a, let kappa_t be the start intensity of components of length at least t. The number of those starts in a deterministic interval of length D is stochastically bounded by Poi(exp(a) kappa_t D). This statement includes components that continue past the interval's right endpoint.

   To see the comparison, explore interval starts and reveal the full interval length at each arrival. At a component end the future process is fresh. The vacant gaps are independent Exp(rho) variables, and successive occupied component lengths are independent marks. Removing occupied lengths moves component starts earlier. The long-component starts in this compressed coordinate form a thinned Poisson process. The exact intensity relation is kappa_t=rho exp(-a) P(B>=t), where B is the length of a fresh component.

2. For any deterministic angular restriction of the isotropic line process, the earlier coverage bound and Campbell's formula give kappa_t<=4 A_mu/t^2. Since a<=4mu, one can use the uniform comparison mean c_mu D/t^2, where c_mu=4 exp(4mu) A_mu.

3. On a deterministic line without an inserted partner, a run start in the intersection of the two angular unions is a component start of at least one union. Assigning each run to such a parent start gives a comparison of all long runs meeting the segment by 1+Poi(2c_mu D/t^2). Independence is used only between the two angular restrictions for that fixed line.

4. For the candidate pairs defined by the intercept and slope constraints, the partner covers the full segment on the base line. Inside that segment, the intersection equals the union of the opposite angular family. Apart from at most two boundary components, long runs are whole components of that opposite union. The same geometric pair intensity as in `corrected-geometry.tex`, followed by two-point Mecke, gives the stated exponential upper bound. The partner is retained after insertion in the Mecke integral.

## A limit of the comparison

The t^(-3) mean run-start density cannot replace the t^(-2) comparison rate in a Poisson bound uniform over segment lengths. On a horizontal line, one angular family has intervals covering an entire segment of length D with probability at least 4mu/(pi D) for sufficiently large D. Independently, the other family has long-component intensity at least 8mu exp(-2mu)/(pi t^2). Its number of complete long components in the segment divided by D converges in probability to that intensity.

Consequently, for fixed t>=4 and all sufficiently large D, the number X_t(D) of run starts satisfies P(X_t(D)>=4mu exp(-2mu) D/(pi t^2))>=2mu/(pi D), although EX_t(D)<=8 A_mu^2 D/t^3. At sufficiently large fixed t, this lower-bound threshold exceeds twice the upper bound on the mean. A Poisson comparison at rate C_mu/t^3 would have an exponential upper tail at the same threshold and is therefore impossible.

This is a proved obstruction to that specific concentration claim. The earlier withdrawn argument used an incorrect individual-interval rate and tried to exclude the larger Km corridor threshold. The new lower bound uses complete connected components and occurs at a smaller threshold. It is fully consistent with the proved exponential upper bound at Km+2.

## What remains

The corridor bound survives a union bound over exponentially many prescribed straight placements. It does not control a path that collects runs while moving between different pairs, since these collections can share underlying lines. The one-line Poisson comparison does not assert that the planar collection of runs is Poisson or independent. A joint estimate for accumulation across changing lines, including short runs and all multiplicities, is still required for the greedy-path criterion. No positive subcritical interval for the original isotropic Cox model follows yet.

The renewal comparison is an application of classical Poisson interval structure. No standalone novelty claim is made for that one-dimensional argument. Its role here is to complete the previously missing connected-run count within the corridor calculation and to identify exactly which stronger concentration claim fails.
