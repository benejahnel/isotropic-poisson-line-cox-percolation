# Uniform control with one common supporting line

The quadratic-insertion test succeeds. The new note `../ordered-corridors.pdf`, with source `../ordered-corridors.tex`, also removes the deterioration of the exponential rate for any number of consecutive corridors sharing one supporting line. The original subcritical theorem remains unproved.

The geometric hypotheses are explicit. The base line in each corridor stays within vertical distance 2 of the common line over a horizontal interval, and these intervals have disjoint interiors in their prescribed order. The vertical condition is used in the proof. Merely assuming containment in the Euclidean strip of radius 2 does not supply this condition in the chosen coordinates.

For r base lines, let p be the number with normal angle below the common angle, let g be the number of nonempty groups on its two sides, and put beta=3r-g. For the sum S of full runs of length at least t meeting the segments, with every distinguished line retained after insertion, Theorem 1.1 gives

    E exp(s S) <= exp(s beta + c_mu D (exp(s)-1)/t^2),  s>=0,

where D is total segment arclength and c_mu is the explicit constant already used in corridor-runs.pdf. Thus, beta<=3r-1, and there is no growing factor in the exponential rate. This is an exponential-moment comparison, without a claim of stochastic domination for restricted component counts.

The deterministic proof starts with an interval J(base,generator) wholly inside one corridor. At its two endpoints the difference between generating and base heights takes the values plus and minus 2 sqrt(1+b_generator^2). Since the base differs vertically from the common line by at most 2, the generator crosses the common line at a horizontal coordinate inside J. Each inserted generator has only one such crossing. Consequently, interior components of inserted intervals can be assigned to distinct generating lines across all corridors. The closest base angle to the common angle on either nonempty side is never an opposite-family insertion, leaving at most r-g assignments. Two boundary runs per corridor give beta.

An interior run disjoint from the inserted intervals is a whole component of the original opposite angular union. Every interval contributing to it has its generating-line intersection with the common line inside that corridor's horizontal range. Therefore, the entire component survives restriction to that set of lines. The sets for different corridors are deterministic and disjoint before tuple selection, giving independent Poisson restrictions.

Deletion can increase component counts, so a stationary count bound cannot simply be applied to these restricted unions. Proposition 2.2 handles this issue by factorial moments. In the multivariate Mecke formula, distinct long components require disjoint background interval chains starting from their respective initial intervals. Van den Berg's Poisson disjoint-occurrence inequality applies to these increasing, bounded-range events for the inhomogeneous restricted process. Each individual extension probability is bounded by its stationary counterpart. The coverage input and the void probability at a component start then give E(X)_k <= (c_mu D/t^2)^k and the stated exponential-moment bound. The full proof checks local finiteness, unique starts, bounded components, measurable restrictions, and the bounded spatial intensity required for the inequality.

For corridor lengths m_i w, M=sum m_i, and w=(t/mu)^(3/2)>=8, the selected-tuple bound is

    P(exists tuple with S>=beta+KM)
      <= G_(m,w) exp(-M Phi(K,epsilon_t)),

with exactly the previous G_(m,w) and epsilon_t. The Mecke integral includes all angular orders together and counts the common line once. Corollary 5.1 also sums over all positive integer compositions of M. With a_t=16mu/(pi w), the probability of any such tuple and composition with S>=(K+3)M is at most

    (mu w/(pi M)) a_t (1+a_t)^(M-1) exp(-M Phi(K,epsilon_t)).

Both losses described in the closing section of joined-corridors.pdf are therefore removed for its ordered corridor geometry. That older note remains a record of a valid weaker argument; its discussion of these losses is superseded. No novelty claim is made for the general use of disjoint occurrence or the Poisson identities.

The common supporting line remains fixed throughout this theorem. When it changes, one random line can belong to restrictions associated with both common lines; the independence proved here then does not follow. A useful next test is a single change of common supporting line, retaining the exact geometry and all inserted lines in the joint Mecke calculation. A full path estimate must also include the remaining reward contributions and multiplicities. The present result establishes neither positivity of the critical Cox point intensity nor submission readiness for a manuscript claiming that conclusion.
