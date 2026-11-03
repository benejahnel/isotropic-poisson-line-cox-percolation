# Joint cost of oscillating corridors

Date: November 3, 2026. The complete statement and proof are in `../oscillating-corridors.tex` and `../oscillating-corridors.pdf`. This is a follow-up to the proposed joint selection calculation in `09-changing-supports.md`.

## Result and scope

For every fixed mu>0 and K>0, choose an integer t>=max(8,4mu) with w/t >= 4096 exp(4mu)(K+4), where w=(t/mu)^(3/2). For all sufficiently large k divisible by 8t, set M=k^2. A prescribed oscillating corridor class contains a tuple with full-run sum at least (K+4)M with probability at least exp(-C k log k). Hence, the unrestricted oscillating extension cannot have an upper tail A exp(-cM), with finite A and positive c, uniformly in M at these fixed parameters.

This conclusion includes the probability cost of choosing the entire tuple. Every other line is retained, and all counts concern full connected components, including components entering from beyond the segment. The construction uses only a fixed subdivision and fixed integer heights within the earlier selection class. It has r=q=k and every nominal corridor has length k widths.

## Geometry and probability cost

Put L=kw, b=1/(4t), H=kw/(8t), epsilon=1/100, and N=floor(H/64). The reference graph starts at height zero and then alternates between H and -H at the horizontal positions iL. Its first slope is b/2; subsequent slopes alternate between -b and b. The midpoint heights are H/2 in the first corridor and zero thereafter.

For each support choose a line whose height at its corridor center differs by at most epsilon from the prescribed midpoint height and whose slope differs from the reference slope by at most epsilon/L. Choose a base by the same height condition, moving the central slope toward zero by 1/L. Choose N additional lines with heights within epsilon of 16j at zero and slopes of absolute value at most epsilon/(kL). For large k these 2k+N sets of lines are disjoint. All selected lines have distinct slopes almost surely.

Each supporting or base set has intensity comparable to 1/L, and each generator set has intensity comparable to 1/(kL), with fixed constants depending on mu,t. Requiring exactly one line in every set has probability

P(E_k)=exp(-nu(U_k)) product_i nu(S_i)nu(B_i) product_j nu(H_j).

Here nu(U_k)=O(1), N=floor(rho k), and rho=w/(512t). Therefore,

log P(E_k)=-(2+2rho)k log k+O_{mu,t}(k).

This includes the angular precision needed to keep each generator nearly horizontal over the full length kL. Actual adjacent support intersections differ from the nominal junctions by at most 12 epsilon t, inside the permitted w/4 ranges. The base-support vertical distance is less than one. No intersection is prescribed at an exact horizontal coordinate.

## Full components in the remaining environment

Every horizontal generator supplies an interval of length at least 8t wholly inside each base segment from the second onward. The active support fills the opposite angular family. Thus, all these intervals lie in the full two-family intersection after restoring the rest of the environment.

For i=4,...,k and j=1,...,N-1, take the point on base i at height 16j+8. These points lie between the generated intervals, inside the segment. Every selected line in the needed angular family is at distance greater than two from each such point. The neighboring generators are eight vertical units away up to a small error; every foreign selected support or base is separated by a distance of order H. The active support belongs to the other angular family.

Conditional on the selected configuration inside the union of the selection sets, the residual process is an independent Poisson process on its complement. The intensity of all lines within distance two of a point is 4mu. Consequently, each midpoint is vacant in the needed family with conditional probability at least p=exp(-4mu).

Let Q=(k-3)(N-1) and let Y count the vacant midpoints. Then E(Y | selected configuration)>=pQ and 0<=Y<=Q, giving P(Y>=pQ/2 | selected configuration)>=p/2. Independence of the vacancy events is neither asserted nor needed. Every vacant midpoint separates distinct full components containing long generated intervals, so the full-run sum S is at least Y.

For large k, pQ/2 >= p w k^2/(4096t) >= (K+4)k^2. Multiplying the conditional probability p/2 by P(E_k) gives the asserted lower bound. This is a full-component argument; possible mergers across the other gaps and extensions outside the segments are allowed.

## Consequence and remaining question

The hoped-for exponential estimate is false for this unrestricted oscillating extension, even after charging every selected line. The previous convex and concave estimates are unaffected because their slope ordering excludes the construction. The theorem concerns the line environment; no Cox points have been sampled, so it does not produce occupied crossings or disprove subcriticality.

The remaining concentration question must permit this subexponential lower bound. One possible target is a weaker upper bound already uniform over the full relevant class, with quantitative constants sufficient for summation across spatial locations and run scales. The present calculation supplies no such upper bound, and an estimate for a single fixed tuple would not resolve the selection problem. The relation between the corridor reward and arbitrary paths, including short runs and multiplicity, also remains to be proved.

No novelty or submission-readiness claim is made for this working note. Its purpose is to settle the specific joint-cost test without extending its negative conclusion to all possible methods.
