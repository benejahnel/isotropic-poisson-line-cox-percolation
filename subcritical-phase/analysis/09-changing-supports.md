# One supporting-line change and repeated changes along a convex graph

The single-change test has a proved upper bound, including a possible jump between the two supporting blocks. The new note is `../changing-supports.pdf`, with source `../changing-supports.tex`. It also proves a uniform bound for arbitrarily many supporting-line changes when their active segments form a continuous convex or concave graph. The full isotropic subcritical theorem remains open.

Let r be the number of base segments and q the number of distinct supporting lines, each used on one consecutive block. All distinguished lines have distinct slopes, and a base line stays within vertical distance 2 of its active support on its segment. The complete run count S includes every other distinguished line after insertion. For q<=2 the allowance B can be taken as 4r+1. For a continuous convex or concave reference graph, any q<=r is allowed and B=4r. In both cases Theorem 1.1 gives

    E exp(s S) <= exp(s B + c_mu D (exp(2s)-1)/(2 t^2)),  s>=0,

where D is total base-segment arclength. The factor two is applied once to the entire sequence. It does not increase with the number of changes in the convex or concave case.

The deterministic argument retains all inserted lines. An interior inserted component contains a generating interval whose line crosses the active support inside that component's horizontal projection. With two supports, each inserted base line can be assigned at most twice, and the two supports together contribute at most one assignment on the opposite block. With a continuous convex or concave graph, each base line crosses the graph at most twice, while an extension of a supporting piece cannot cross another piece in its interior. The two endpoint runs per base segment then give the stated allowances.

Every other interior run survives restriction to lines crossing its active supporting segment in its horizontal range and belonging to its opposite angular family. With two supports, these restrictions are disjoint within each supporting block. With a convex or concave graph, they are disjoint within each of two collections classified by whether the base angle lies below or above its support angle. A generating line has at most one crossing of each direction. The restricted component estimate from ordered-corridors.pdf applies to each count; independence within a collection and one application of Holder's inequality between the two collections prove the moment bound.

Corollary 4.1 includes selection of the distinguished lines from the Poisson process. Each distinct support is inserted once, even if many base corridors use it. For continuous chains, junctions between distinct supports are their actual intersections, allowed to move within intervals of width w/2 around nominal grid boundaries. These conditions have positive width. No exact equality at a predetermined junction coordinate is imposed on independent Poisson lines.

With w=(t/mu)^(3/2), t>=max(8,4mu), M=sum m_i, and epsilon_t=4 c_mu w/t^2, the fixed-choice tail is

    P(exists selected tuple with S>=4r+KM)
      <= G_(m,k,w) exp(-M Phi(K,epsilon_t)/2).

Here M_j is the total nominal length in widths of supporting block j and

    G_(m,k,w) = (mu w/pi)^q (32 mu/(pi w))^r
                 / (product_j M_j product_i m_i).

For two supporting blocks with fixed junction coordinates, the same bound holds at 4r+1+KM without convexity or continuity. For the continuous convex or concave class, the union over all integer compositions, all consecutive block partitions, and all allowed integer vertical coordinates has the bound

    P(S>=(K+4)M for some eligible choices)
      <= 3^M a_mu (1+2a_mu)^(M-1) exp(-M Phi(K,epsilon_t)/2),

where a_mu=32 mu^2/pi^2. At fixed mu and K>0, its exponential rate can be made arbitrarily large by increasing t.

The remaining geometric restriction is substantive. Section 5 constructs an oscillating polygonal graph and base lines satisfying the same vertical-distance bound such that one horizontal generating line contributes an interior interval longer than t in every corridor. A whole open set of generating lines has this property for each fixed number of pieces. Thus, the number of effective Poisson restrictions sharing a line is unbounded for unrestricted turns. This is an obstruction to the uniform overlap count used in this proof. It is not a lower bound contradicting concentration after selection of an oscillating supporting tuple, and it is not a proof against the original subcritical claim.

The next concrete test is to retain the probability cost of oscillating supporting tuples together with the generating lines that they repeatedly use. One should integrate these geometries jointly before replacing the conditional probability by a worst-case fixed-tuple bound. Such an argument must continue to include complete connected runs assembled from several shorter intervals. A count of isolated long intervals would not settle the remaining path problem.

The seven-page note uses the previously proved restricted component estimate as a fully stated input, and gives complete proofs of the new geometric reduction, exponential bound, selection estimate, and overlap example. No independent novelty audit or submission-ready subcritical theorem is asserted.
