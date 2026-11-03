# Dyadic estimate: corrected assessment, November 3, 2026

The previous claimed obstruction is withdrawn. Its rate calculation confused the number of intervals with the total length they cover. See `../corrected-geometry.tex` and its compiled PDF for the complete proof replacing that calculation.

For a fixed line and t>=8, the rate of intervals of length in [t,2t] is
q_t=(2mu/pi)(sqrt(1-4/t^2)-sqrt(1-16/t^2)) <= 5mu/t^2.
The expected number of such intervals covering a fixed point is
b_t=(8mu/pi)(arcsin(4/t)-arcsin(2/t)) <= 6mu/t.
The number meeting a segment of length D is Poisson with mean q_t D+b_t.

For a row of length L=mw and width w, the specified first lines have intensity of order mu w^2/L, and their close partners have intensity of order mu/L. The product intensity of the ordered pairs is therefore of order mu^2/m^2. An upper bound with constant 16/pi^2 is proved for the explicit intercept and slope ranges in the correction note.

At w=(t/mu)^(3/2), the mean number of additional intervals per pair is at most m epsilon_t, with epsilon_t=10/sqrt(mu t)+6mu/t. The Mecke formula followed by the Poisson Chernoff bound gives an exponential upper bound in m at every sufficiently large t, uniformly over all pairs satisfying those geometric constraints. Thus, the previous argument using a single long pair does not give the claimed polynomial lower bound at large scales.

The positive result does not control the full number of maximal connected runs. Runs may be formed by chains of shorter intervals, or by intersections of longer intervals, and the lattice set is only covered by the continuous construction. The heuristic density mu^3/t^3 for maximal runs has not been proved. Shared-line estimates do not imply disjoint line families, and bounds for single pairs do not control paths that visit many pairs.

The former dyadic synthesis also left the additive terms at large scales untreated. Their sum cannot be declared o(n) without a separate estimate. The ranges of the size and location of connected sets must be specified before applying an exponential union bound.

The correct current verdict is that this dyadic route remains unresolved. The calculation supplies a positive bound for a specific contribution, and removes the earlier stated reason for rejecting that contribution. It proves neither a subcritical phase nor that every other obstruction can be overcome.
