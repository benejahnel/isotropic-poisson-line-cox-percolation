# Connected-run estimate: completed step

Full statement and proof: `../connected-runs.pdf` and `../connected-runs.tex`.

Theorem 1.1 bounds runs in the intersection of the two angular interval unions. The bound includes arbitrary concatenations, multiplicity over lines, and components entering the region from outside. Corollary 1.2 supplies an almost-sure bound on the largest component meeting a growing square.

The main estimate is E M_t(K) <= B_mu mu (area(K)/t^3 + perimeter(K)/(pi t^2)), where B_mu is finite for every mu and B_mu=8(192mu)^2 for 0<mu<=1/32. The component-start bound omits the boundary term. The square exponent 2/3+epsilon follows by Markov's inequality and Borel--Cantelli on dyadic radii.

The proof does not assume that long components consist of single long intervals. It bounds whole-segment coverage using the recursion u(3t)<=u(t)^2+6mu/t, then squares the result using the independent angular families. A stationary component identity converts coverage probability into component-start intensity, and a one-line Mecke formula handles lines drawn from the environment.

The remaining obstruction is neither an infinite finite-path exponential moment nor the former claimed polynomial overload from one pair. It is the absence of a proved uniform bound for the weighted component sum along all admissible paths. Correlated components and the short-component contribution must still be treated. The subcritical theorem is not proved.
