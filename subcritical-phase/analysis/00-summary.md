# Current status after occupied passage through oscillating corridors: November 3, 2026

The occupied-passage test has matching upper and lower probability orders for the prescribed oscillating tube, with the full remaining environment restored. Start with `../occupied-corridors.pdf` and `../occupied-corridors.tex`. The original isotropic subcritical theorem remains open.

For every fixed positive point intensity lambda and the parameters of the previous construction, write M=k^2 and R=k^2 w. Conditional on the original selected lines, the probability of an occupied passage through the tube of vertical half-width 2 following their continuous supporting graph lies between exp(-C k (log k)^2) and exp(-c k (log k)^2). The lower bound also requires the original large full-run event S_k >= (K+4)k^2. After including the original selection event E_k, the joint probability has the same order. All constants are uniform over the original selected configuration at fixed parameters.

The upper bound allows every route within the tube, including disks centered outside it and all remaining lines. Separating rectangles reduce passage to occupancy of every rectangle. One line contributes at most 5kw total arclength to them; the corresponding Poisson integral has second moment bound O(mu n log n), where n is of order k^2w. The Poisson exponential formula and conditional independence of Cox counts give the upper bound. The lower bound adds order log k nearly parallel lines along each of the k supporting segments. These lines can carry the passage while leaving a positive fraction of the original separating points vacant in the opposite angular family, preserving distinct full components.

The selected lines alone have an exponential upper bound in R when lambda<1/28, because their local line multiplicity is at most seven. Restoring the remaining environment permits the additional line groups used in the lower bound. Thus, the complete occupied-passage cost has order sqrt(M)(log M)^2 in its negative logarithm and cannot satisfy an upper bound A exp(-aM).

This is a precise estimate for one prescribed construction, not a phase transition theorem. Its upper bound is summable over k, but it is not uniform over every possible tube selected from the environment, and the path is confined to the stated tube. Because the estimate holds for every fixed lambda>0, it does not distinguish phases. The remaining task is control of the family of relevant paths and their selection costs. See `11-occupied-corridors.md` for the complete assessment.

## Earlier assessment after the joint oscillation calculation

# Current status after the joint oscillation calculation: November 3, 2026

The joint calculation rules out the proposed exponential upper tail for the unrestricted oscillating extension of the corridor class. Start with `../oscillating-corridors.pdf` and `../oscillating-corridors.tex`. The original isotropic subcritical theorem remains open.

For every mu>0 and K>0, take a sufficiently large fixed integer t and put w=(t/mu)^(3/2). The precise condition is w/t >= 4096 exp(4mu)(K+4). Along M=k^2 with k divisible by 8t, the probability that some eligible tuple has full-run sum at least (K+4)M is at least exp(-C sqrt(M) log(M)). This contradicts every proposed uniform upper bound A exp(-cM), with finite A and c>0, at these fixed parameters. It already holds on one prescribed subdivision and one prescribed integer sequence of vertical positions.

The construction uses k supporting lines, k base lines, and N=floor(rho k) nearly horizontal generators, where rho=w/(512t). The exact joint Poisson selection calculation gives log P(E_k)=-(2+2rho)k log k+O(k). These generators create long intervals on order k base segments. In the remaining environment, each separating midpoint stays vacant in the needed angular family with conditional probability at least exp(-4mu). An expectation bound, requiring no independence between midpoints, preserves a positive fraction with positive probability. The result therefore counts distinct full components after every remaining line is restored.

This closes the specific proposal that paying jointly for the oscillating supporting tuple and its repeatedly used generators might recover an exponential tail in M. It leaves the convex and concave estimates intact. It neither disproves positive critical Cox intensity nor rules out a suitable almost-sure bound on environmental reward. A weaker uniform upper bound could still be useful if its decay and constants suffice across locations and run scales. No such upper bound for the full class, or passage to arbitrary relevant paths, is established here. A summable lower bound alone gives no upper summability statement.

See `10-oscillating-corridors.md` for the construction, exact probability calculation, and remaining question.

## Earlier assessment after changing the supporting line

# Current status after changing the supporting line: November 3, 2026

The next test succeeds for a single supporting-line change, including a jump between the two blocks. It also gives a uniform estimate through arbitrarily many changes when the active supporting segments form a continuous convex or concave graph. Start with `../changing-supports.pdf` and `../changing-supports.tex`. The original subcritical theorem remains open.

For r base corridors, the full-run sum S has exponential moment at most exp(s B + c_mu D (exp(2s)-1)/(2t^2)). A single change permits B=4r+1. A continuous convex or concave reference graph permits B=4r for any number of distinct supporting lines. The factor two in the exponential rate is incurred once for the whole sequence and does not grow with the number of changes in this class.

The deterministic proof counts all inserted lines through their intersections with the active supporting segments. For a convex or concave graph, every inserted base line contributes at most two interior assignments and supporting lines contribute none. The remaining counts split into two collections of independent Poisson restrictions according to crossing direction. The already proved component estimate under deterministic restrictions then applies, followed by one use of Holder's inequality.

The selected-tuple estimate uses actual moving junctions and the multivariate Mecke formula, inserting every distinct supporting line once. Corollary 4.1 also sums over every integer composition of a fixed total horizontal range, every consecutive grouping of bases by support, and an exponentially large family of vertical positions. The resulting exponential rate remains arbitrarily large at sufficiently large run threshold t.

Unrestricted oscillation remains open. An explicit example shows that a positive-intensity set of generating lines can affect every corridor of an oscillating chain, even with long intervals wholly inside the segments. This only disproves a uniform bound on reuse of those lines under the stated geometry; it does not disprove a subcritical phase or another concentration argument. The next test is to estimate oscillating supporting tuples jointly with the repeatedly used generating lines, retaining their geometric probability cost and the full connected-run construction. See `09-changing-supports.md` for the exact results and remaining scope.

## Earlier assessment after the ordered-corridor estimate

# Current status after the ordered-corridor estimate: November 3, 2026

The quadratic insertion allowance has been reduced to a linear one. The same geometric observation, together with a component-count estimate under deterministic restrictions, also removes the growing loss in the exponential rate. Start with `../ordered-corridors.pdf` and `../ordered-corridors.tex`. The full isotropic subcritical problem remains open.

For r consecutive corridors satisfying the prescribed vertical-distance bound and sharing one common supporting line, the total full-run count S has exponential moment at most exp(s beta + c_mu D (exp(s)-1)/t^2), where beta=3r-g<=3r-1, D is total arclength, and g is the number of nonempty angular groups on either side of the shared angle. Every inserted line is retained. The proof charges interior inserted components to distinct intersections with the common line, and separates the remaining components into independent restrictions according to their intersection coordinates on that line.

The bound under deterministic restrictions requires a new argument because deleting intervals can increase component counts. The proof uses factorial moments and van den Berg's Poisson disjoint-occurrence inequality for the finite background chains realizing distinct long components. The stationary coverage estimate supplies the extension probability. This gives an exponential-moment comparison with the same c_mu as before, without asserting stochastic domination for restricted counts.

Theorem 1.1 handles supporting tuples selected from the environment, with upper bound G exp(-M Phi(K,epsilon_t)) at beta+KM and no factor depending on r in the exponent. Corollary 5.1 sums over all integer subdivisions of a fixed horizontal range, at threshold (K+3)M. Both previous growing losses are removed for this class of ordered corridors. The hypotheses include vertical distance at most 2 from the common line; Euclidean strip containment alone is insufficient for this proof in the stated coordinates.

The next unresolved change is a change of the common supporting line itself. Independence of the restrictions then no longer follows, since one random line can cross both common lines in their respective active ranges. The natural next test is one such change with the full joint insertion calculation. The remaining path reward and multiplicity estimates must also be supplied before a subcritical theorem follows. See `08-ordered-corridors.md` for the detailed record.

## Earlier assessment after the joined-corridor test

# Current status after the joined-corridor test: November 3, 2026

The two-corridor test is complete, and the same argument has been checked for repeated joins around one shared supporting line. Start with `../joined-corridors.pdf` and its source `../joined-corridors.tex`. The original isotropic subcritical problem remains open.

The new result treats actual connected runs on different base lines and retains all inserted lines in the covering. Let r corridors share one supporting line, with p base-line angles below its angle and r-p above. Set q=max(p,r-p) and b=2r+choose(p,2)+choose(r-p,2). For a fixed tuple with total segment length D, the exponential moment of its total run count S is at most exp(s b + c_mu D (exp(q s)-1)/(q t^2)). The groups below and above the shared angle use disjoint Poisson angular restrictions; dependence within a group is handled by Holder's inequality.

For consecutive prescribed corridors of lengths m_i w, where w=(t/mu)^(3/2)>=8 and M=sum m_i, Theorem 1.1 bounds the probability of a tuple selected from the environment having S>=b+KM by G exp(-M Phi(K,epsilon_t)/q). Here epsilon_t=2c_mu w/t^2 and G=16^r mu^(r+1) w^(1-r)/(pi^(r+1) M product(m_i)). The factor G follows from one shared-line intensity and r conditional base-line intensities; the shared line is not counted twice.

For two corridors, the shared angle lies between the base angles when p=1. Then q=1 and b=4, so the exponential rate is preserved. If both base angles lie on one side, q=2 and b=5. Thus, a useful two-corridor bound is established in every angular case, including selection of the triple from the environment.

The repeated-join constants do not remain uniform in this proof. For any angular split, q>=ceil(r/2) and b>=r^2/4+3r/2. The geometric prefactor also helps in suitable regimes, but these estimates have not yielded the required linear path bound. Neither the rate loss nor the quadratic insertion allowance has been proved necessary. This is not a new impossibility result for the underlying path problem.

There is a uniform bound when the base line stays unchanged. For any partition of a fixed segment of length D into r consecutive pieces, even chosen measurably after observing the environment, the sum of the run counts over the pieces is bounded by r+Poi(2c_mu D/t^2). The deterministic reason is that each internal partition point can duplicate at most one run. The Poisson comparison then applies once on the whole segment.

What remains is a uniform estimate across an unbounded number of genuine changes of base line, with overlapping angular families, inserted-line effects, short runs, and all multiplicities retained. The earlier results on connected-run lengths and straight corridors remain valid. Positivity of the critical Cox point intensity is still unproved.

## Earlier assessment after the corridor estimate

The proposed upper-tail investigation is complete for a straight corridor supported by one nearly parallel pair. Start with `../corridor-runs.pdf`, whose complete proof is in `../corridor-runs.tex`. The full subcritical problem remains open.

Theorem 1.1 now controls complete connected runs, including arbitrary chains of shorter intervals. For a corridor of length m w and width w=(t/mu)^(3/2), the probability that some candidate pair supports at least Km+2 runs of length at least t is at most (16 mu^2/(pi^2 m^2)) exp(-m Phi(K,epsilon_t)). Here epsilon_t=8 exp(4mu) A_mu/(mu^(3/2) sqrt(t)) and Phi(K,u)=K log(K/u)-K+u. Thus, the bound is exponential in m with an arbitrarily large rate at sufficiently large t, for fixed mu and K. It can handle an exponentially large prescribed family of straight corridor placements by a union bound.

The main input is a Poisson comparison for one angular family. If kappa_t is its intensity of component starts with lengths at least t and a its mean coverage multiplicity, then the number of such starts in length D is stochastically bounded by a Poisson variable of mean exp(a) kappa_t D. Deleting all occupied portions leaves exponential vacant gaps and independent component-length marks. Coverage estimates give kappa_t <= 4 A_mu/t^2 and a <= 4mu. The two-point Mecke formula handles pairs selected from the environment while retaining their contribution to the covering.

Proposition 4.1 identifies a genuine obstruction at a different threshold. On a horizontal deterministic line, EX_t(D)<=8 A_mu^2 D/t^3 for the number of long run starts. Yet for delta_t=4mu exp(-2mu)/(pi t^2), P(X_t(D)>=delta_t D)>=2mu/(pi D) for every sufficiently large D at fixed t>=4. This rules out a Poisson comparison with mean C_mu D/t^3, even with a fixed finite additive boundary term, uniformly over t and D. It does not contradict the corridor bound: at the proposed corridor width, this lower-bound threshold is of order m/sqrt(mu t), below Km at large t.

What remains is control of the total reward accumulated by paths that change supporting lines or pairs, with all shared-line dependence and short-run contributions retained. Neither independence between different corridors nor a full path estimate has been established. The current results are proved inputs and a limitation of one concentration claim, not a proof that all approaches fail and not a subcritical theorem.

## Earlier assessment after the connected-run estimate

The fixed-line component-length estimate has now been proved for the continuous covering used in the isotropic model. The full subcritical problem remains open. Start with `../connected-runs.pdf`, whose complete proof is in `../connected-runs.tex`.

For each fixed line, the probability that one angular family covers a segment of length t is at most A_mu/(1+t). This bound includes every chain of shorter intervals. It follows from a vacancy estimate at one scale and the recursion u(3t)<=u(t)^2+6mu/t. For mu<=1/32 one may take A_mu=192mu.

The two angular families are independent. Stationarity then bounds the intensity of complete runs of length at least t by 8A_mu^2/t^3 per unit arclength. The Mecke formula integrates this over the random lines, retaining multiplicity. The expected number of run starts in K is at most 8mu A_mu^2 |K|/t^3. For a convex region, the expected count of runs meeting K also has the boundary term 8mu A_mu^2 perimeter(K)/(pi t^2). These are upper bounds, with no claim of matching asymptotics.

The longest run meeting [-n,n]^2 is O(n^(2/3+epsilon)) almost surely, for every epsilon>0. Thus, for epsilon<1/3, the additive terms in the dyadic decomposition sum to o(n). This supplies the large-scale remainder that was missing from the preceding analysis.

What remains is a uniform linear bound on the weighted sum of runs visited by arbitrary admissible paths, including short runs and multiplicities. The first-moment density bound does not imply that maximum bound because different runs can depend on common lines. No positive range of point intensities without percolation has yet been established.

The proof uses elementary Poisson coverage, stationarity, and the Mecke formula. It is a proved input for this approach, rather than a claim of a new standalone theorem in one-dimensional Boolean percolation.

## Earlier assessment, superseded where indicated above

# Current status: November 3, 2026

Positivity of the critical point intensity remains unproved, including in the sparse regime. The revised sources and the fully proved correction note supersede the earlier claims about infinite finite-path moments and the dyadic obstruction.

The new result is Proposition 1.1 of `corrected-geometry.pdf`. For the precisely specified candidate pairs, the probability that some pair has at least Km additional intervals of length in [t,2t] meeting its segment is at most C mu^2 m^{-2} exp(-m Phi(K,epsilon_t)), where epsilon_t=10/sqrt(mu t)+6mu/t. In particular, it is at most C mu^2 m^{-2} 2^{-Km} at sufficiently large t. The proof includes intervals entering the segment and uses the two-point Mecke formula to handle selection of the pair from the environment.

The claim that a finite straight path has an infinite exponential moment was false. The corrected moments are finite, while their logarithms grow faster than linearly in the path length. The direct annealed path-sum bound and the elementary count of many paths on the same rare collection of lines still fail to provide the required estimate.

The former dyadic lower bound used mu/t instead of mu/t^2 for the interval rate and included an erroneous extra factor of the box width in the pair calculation. Its proof is withdrawn. The corrected upper bound concerns individual intervals; it does not establish the required bounds for maximal connected runs or for paths visiting many pairs.

The small-mu expansion of the greedy growth constant, the stated density of maximal runs, and the claim that distant configurations use disjoint lines are not established. The earlier implication that a particular hierarchical induction is necessary is also withdrawn.

The next precise mathematical task is to control connected components of the intersections of the two interval unions on a line, retaining the multiplicities needed for the lattice reward and handling the dependence when paths select and visit many lines. A complete proof also needs a treatment of the largest scales and boundary-crossing components.

Files `01-review.md`, `02-greedy-conjecture.md`, and `03-sparse-regime.md` retain the historical analysis with an explicit status notice. They should not be treated as independent verification of the revised results. File `04-plan-step1.md` now records the corrected assessment.
