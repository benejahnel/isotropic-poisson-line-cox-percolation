# Occupied passage through the oscillating configuration

Date: November 3, 2026. The full statement and proof are in `../occupied-corridors.tex` and `../occupied-corridors.pdf`. This completes the proposed test of sampling Cox points and retaining the surrounding environment.

## Main result

Use the original selection cells and event E_k from `10-oscillating-corridors.md`, with all parameters fixed and k divisible by 8t. Let G_k contain the original selected line configuration. The supporting pieces form a continuous graph g on [0,R], where R=k^2w and M=k^2. The passage event C_k requires a continuous occupied curve from x=1 to x=R-1 inside |y-g(x)|<=2. All lines and all Cox points are retained; centers outside the tube may contribute disks. Let F_k be the original full-run event S_k >= (K+4)k^2, evaluated in the complete line environment.

For every fixed lambda>0, there are positive c,C and k_0 such that, on E_k and for k>=k_0,

P(F_k intersection C_k | G_k) >= exp(-C k (log k)^2),
P(C_k | G_k) <= exp(-c k (log k)^2).

The joint probability P(E_k intersection F_k intersection C_k) also lies between bounds of these two orders. The previous cost log P(E_k)=-(2+2rho)k log k+O(k) is smaller in magnitude and can be absorbed into the constants. No independence between F_k and C_k is claimed. Their lower bound uses a specific independent source of Cox points after fixing the additional lines.

## Upper bound with the full environment

Choose n=floor((R-2)/32) separating rectangles of width 2 and height 6, centered at (32j,g(32j)). If any rectangle has no Cox point, its vertical section through the tube is vacant and no passage exists. The rectangles are disjoint. Conditional on every line, their point counts are independent, even though their directing arclengths are dependent.

The original selected lines have local multiplicity at most seven in every disk of radius four centered in the horizontal range. Thus, their arclength in a separating rectangle is at most 56. Any additional line contributes at most B=5kw to all the rectangles together. To prove this, contain the rectangles in a tube of vertical half-width five around the nominal oscillating graph. A line whose slope differs substantially from both alternating slopes has a bounded contribution to each piece. A line close to one alternating slope can meet at most one of the corresponding pieces for a long distance, because those pieces are widely separated in height at their centers. The total arclength is at most 4L+40k/b <= 5kw.

Let T be the residual arclength summed over the rectangles. Its conditional mean is at most 12mu n. Its Poisson variance parameter is at most v=1024mu n(1+log n). The variance estimate follows from the bound 8mu/(pi |i-j|) on the intensity of lines meeting two radius-four disks centered at the corresponding rectangles.

The exponential formula gives log E exp(s(T-ET)) <= (v/B^2)(exp(sB)-1-sB). Choose s=(log k)/B and separate the event T>12mu n+n log k/(2lambda). On its complement, the probability that all rectangles receive points is at most exp(-q n/sqrt(k)), where q=exp(-lambda(56+12mu)). The exceptional probability is at most

exp(-n(log k)^2/(2lambda B)+(v/B^2)(k-1-log k)).

For large k their sum is at most 2 exp(-k(log k)^2/(1280lambda)). This bound is uniform over the initial selected lines and allows all routes in the tube.

## Lower bound and preservation of full runs

For each selected support g_i, choose a residual line group with center height near g_i(c_i)+1/2 and slope within delta/L of the support slope, with delta=1/100. These line sets are disjoint from each other and from the original selection sets. Each has intensity between 4mu delta^2/(3pi L) and 4mu delta^2/(pi L).

Require exactly J lines in each group, with J=ceil(16 log(m+2)/lambda) and m=ceil(2(R-3)). There are m+1 squares of side 1/4 following the continuous graph g+1/2, with horizontal spacing at most 1/2. Every line in the active group contributes at least 1/8 arclength to the corresponding square. A union bound shows that all squares receive Cox points from these groups with probability at least 1/2. The chosen centers and two end points form an occupied polygonal path that stays in the tube.

These extra groups also permit the original full-run event. On their own base they lie in the same angular family as the active support. At the original separating midpoints on foreign base segments, they are at distance greater than two. Conditional on all original and additional selected lines, the remaining Poisson process leaves each midpoint vacant in the needed family with probability at least p=exp(-4mu). The expectation argument from the previous construction therefore gives P(F_k | these lines)>=p/2. This argument counts full components after restoring all lines and permits mergers across the other gaps.

The point event uses only the additional groups, while the vacancy event depends only on the remaining lines. Conditional on the fixed groups, these sources are independent. Thus, the joint conditional probability is at least p/4 times the probability of choosing the additional groups. Since J/log k tends to 32/lambda, the latter has negative logarithm at most (32/lambda+o(1))k(log k)^2. This proves the lower bound with the full-run event retained.

## Selected lines alone

Every disk of radius two in the slab has selected arclength at most 28. For lambda<1/28, the multivariate Mecke formula bounds ordered chains of d centers by a starting intensity times (28lambda)^d. An occupied passage requires at least d=ceil((R-4)/2) edges, giving

P(C_k selected only | G_k) <= 2 sqrt(2) lambda (2k+N) (28lambda)^d.

This is exponential in R. The full-environment lower bound shows why deleting the remaining lines would give the wrong probability scale for the original question.

## Consequence and limitation

The occupied-passage test is now settled for this prescribed tube. Sampling Cox points changes the negative logarithm from order k log k for the original selected environment to order k(log k)^2 for a joint configuration with passage and many full runs. The full cost is still sublinear in M=k^2, so an exponential upper bound in M cannot be recovered by including point costs.

The positive upper bound is summable over k for this construction, and it explicitly includes the residual environment. It does not provide a uniform bound over the family of possible selected tubes, nor allow a path to leave the tube and return. It holds for every fixed positive lambda and therefore does not establish a phase transition or a new subcritical variant. The remaining mathematical issue is control of adaptive route selection and its multiplicity at the relevant spatial scales. No claim that all methods are exhausted, or that the original subcritical manuscript is submission-ready, follows from this calculation.
