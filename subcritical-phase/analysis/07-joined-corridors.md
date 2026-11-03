# Joined corridors sharing a supporting line

The proof is in `../joined-corridors.tex`, rendered as `../joined-corridors.pdf`. It uses the one-family Poisson comparison from Proposition 2.1 of `../corridor-runs.pdf`, restated in full as Lemma 3.1 of the new note.

## Fixed-tuple estimate

Take a shared supporting line ell_0 and r distinct base lines ell_i. Segment I_i lies on ell_i and is contained in J(ell_i,ell_0), the portion within distance 2 of the shared line. The run count on each base uses the original Poisson environment together with all the other distinguished lines. Let S be the sum of these run counts for components of length at least t.

For base i, the shared line supplies the angular family toward its own angle throughout I_i. The remaining family A_i lies below the base angle when that angle is below the shared angle, and above it when it is above. Let Y_i count long component starts in I_i from the original environment restricted to A_i.

Adding a single interval can increase the number of long components with starts in a fixed segment by at most one: every affected component is replaced by a single merged component. Therefore, H_i<=2+h_i+Y_i, where h_i counts the other distinguished base lines in A_i. The term 2 includes both endpoint components. If p base angles are below the shared angle, then sum h_i=choose(p,2)+choose(r-p,2).

The lower-angle group of Y_i and the upper-angle group are independent as entire groups. The counts within each group can be dependent. Holder's inequality within each group and the one-family Poisson comparison yield

    E exp(s S) <= exp(s b + c_mu D (exp(q s)-1)/(q t^2)),
    q=max(p,r-p),
    b=2r+choose(p,2)+choose(r-p,2),

where D is the sum of the segment lengths. Empty groups contribute the factor one. The estimate is uniform over every deterministic tuple satisfying the stated strip containment.

## Selection from the environment

The shared line crosses a rectangle of length M w and width w. Base line i stays within vertical distance 2 of it over the consecutive subinterval of length m_i w, with M=sum m_i. Consecutive base endpoints are at most distance 4 apart. This specifies geometric proximity, without assuming an occupied Cox connection at the join.

For w>=8, each base segment has arclength at most 2m_i w. The product intensity of eligible tuples is at most

    G=16^r mu^(r+1) w^(1-r)/(pi^(r+1) M product(m_i)).

The shared line contributes mu w/(pi M), and each base contributes 16mu/(pi m_i w). The multivariate Mecke formula retains the entire tuple in the tested covering. With w=(t/mu)^(3/2), epsilon_t=2c_mu w/t^2, and K>epsilon_t, the probability that some eligible tuple has S>=b+KM is at most

    G exp(-M Phi(K,epsilon_t)/q).

Here Phi(K,u)=K log(K/u)-K+u. This is Theorem 1.1 of the note.

## What succeeds for two corridors

When the shared normal angle lies between the two base angles, p=1, q=1, and b=4. The two opposite angular families are disjoint; the joint exponential rate is preserved. When both base angles lie on one side, q=2 and b=5, giving a factor of two lost in the exponent. In either case the rate can be made arbitrarily large at fixed mu and K by increasing t. Thus, a union bound over exponentially many prescribed placements of two joined corridors is available.

## What happens under repetition

For r base lines around the same shared line, q>=ceil(r/2) and b>=r^2/4+3r/2. Hence, the argument does not retain uniform constants as the number of base lines increases. With m_i=1, the additive allowance is already quadratic in the total number M=r of corridor widths. The prefactor G also decreases in useful regimes, but no uniform path estimate has been deduced by combining it with these bounds.

These losses come from Holder's inequality and from counting all possible insertion effects separately. We have not proved them optimal or established a counterexample to better joint concentration. In particular, this result must not be described as proving that every iteration or every subcritical approach fails.

For one unchanged deterministic base line, all consecutive subdivisions of a fixed segment can instead be handled together. Each partition point duplicates at most one run. Thus, the sum of the counts over r pieces is stochastically bounded by r+Poi(2c_mu D/t^2), even if the partition is chosen measurably after the environment is seen. The fixed segment and r are specified in advance. The remaining problem is the accumulation across genuine changes of base line.
