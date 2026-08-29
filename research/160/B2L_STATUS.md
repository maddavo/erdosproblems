# B2-L working status

## Purpose

After Branch A, the degree-\(\le5\) polynomial search is restricted to genuinely coupled quintic top forms

$$
F:=Q_5\ne\lambda L^5.
$$

The B2-L subbranch is the persistent **linear-factor** case for the intersection of the first polar and the Hessian/third polar.

The goal is to show that no such \(F\) can support an ABBA-free scalar colour map on \(\mathbb F_p^5\).

This file records the working proof tree. Many entries are detailed working eliminations rather than publication-audited theorems.

## Basic polar geometry

For a fixed nonzero step \(h\), the two ABBA equations can be written as a quartic and a quadratic equation in the centre \(x\):

$$
A_h(x)=0,\qquad B_h(x)=0.
$$

Their leading parts depend only on \(F\):

$$
A_h^{(4)}=D_hF,\qquad B_h^{(2)}=D_h^3F.
$$

The third polar satisfies

$$
D_h^3F(x)=3\,\operatorname{Hess}F(h)[x,x].
$$

If, for some \(h\), the projective complete intersection

$$
D_hF=D_h^3F=0
$$

is geometrically integral, then Lang–Weil gives an \(\mathbb F_p\)-point for sufficiently large \(p\), hence a bad AP.

Therefore an asymptotic survivor must be geometrically exceptional for every relevant \(h\).

## Generic B2 elimination

For generic genuinely coupled \(F\), there are directions \(h\) for which the quartic first polar and the Hessian quadric meet transversely/geometrically integrally. Hence generic \(F\) is excluded.

Working conclusion:

$$
\text{only a proper algebraic exceptional locus of quintics can survive.}
$$

## B2-L factor pattern

On a dense open set of directions, non-integrality of the degree-\((4,2)\) intersection forces a factor pattern on the Hessian quadric.

The linear-factor branch is denoted B2-L:

$$
D_hF=L_hC_h+(D_h^3F)G_h.
$$

The complementary quadratic split is B2-Q and has not yet been the main focus.

## Moving hyperplane degree

A multidegree argument shows that, away from vertical Hessian-rank pathologies, the rational map

$$
h\mapsto[L_h]
$$

has projective degree at most 1.

- Degree 0: fixed hyperplane.
- Degree 1: bilinear moving hyperplane.

The fixed and bilinear cases were treated as impossible.

### Fixed hyperplane

The fixed case forces the quintic top into a form with a linear factor (in stronger working reductions, \(F=L^2H_3\)). Centred-direction and local Frobenius-branch arguments then give bad directions.

### Bilinear moving hyperplane

If

$$
L_h(x)=B(h,x),
$$

the factor identity forces

$$
D_hF=B(h,x)C(x).
$$

Thus every first derivative of \(F\) has a common cubic factor. Degree considerations then force \(F\) to depend on at most two linear forms, so

$$
\det\operatorname{Hess}F\equiv0,
$$

contradicting B2.

## Vertical exceptional divisors

The only way the degree argument can fail is on a divisor of \(h\)-space where the Hessian quadric degenerates enough to absorb the moving hyperplane.

This led to classification by the degree of the exceptional divisor \(B\).

### Degree 1

Linear-factor cases were eliminated by centred ABBA arguments.

### Degree 2: quadrics

Working proof eliminated all irreducible quadric ranks:

- rank 5 smooth quadric;
- rank 4 cone;
- rank 3 cone.

Rank 1/2 cases are reducible/nonreduced and reduce to linear-factor geometry.

Status: **working elimination**.

### Degree 3: cubics

The working proof treated, in succession:

- smooth cubics;
- factorial normal isolated cubics;
- non-\(\mathbb Q\)-factorial plane cases;
- cubic-scroll cases;
- nonnormal Perazzo-type cubics;
- cubic cones;
- normal cubics singular along a line;
- normal cubics singular along a conic;
- the chordal cubic singular along a rational normal quartic.

The chordal case used the secant-resolution geometry and a symbolic-power calculation on the rational normal quartic.

Working conclusion:

$$
\text{degree-3 exceptional divisors are eliminated.}
$$

Status: **working elimination — requires systematic audit.**

### Degree 4: quartics

This is the active branch at the documentation stop.

Already treated in the working proof:

- low-span line/conic polar images: eliminated by constant relations;
- factorial quartic exceptional divisors: eliminated;
- degree-4 del Pezzo fibre \(A=V(q_1,q_2)\): working algebraic exclusion;
- degree-5 del Pezzo fibre: substantial exact computation and geometric reduction.

#### Degree-5 del Pezzo correction

An earlier conjecture that the directional-derivative degeneracy locus was exactly the del Pezzo surface was found to be false.

Correct picture:

- ordinary projection centres: no double quintic found;
- centres on one of five Segre threefolds associated with conic pencils: a 7-dimensional space of double quintics appears;
- centres on the del Pezzo itself: larger kernel, but the projection degree changes.

For special Segre centres, the projected \(dP_5\) lies on a rank-4 quadric \(q\), and every degree-5 polynomial singular along the projected surface is divisible by \(q\). The B2 Hessian rank condition then forces the constant polar direction into the normal span, contradicting nondegeneracy of the fibre.

Working conclusion: degree-5 del Pezzo fibres appear eliminated, but one invariant Pfaffian/degeneracy-locus lemma still deserves formal packaging.

## Exact current resume point

The last active idea before the user stopped the mathematics was:

> Attack the remaining nonfactorial / sufficiently singular quartic threefold by classifying the possible low-degree generic polar fibres.

A proposed simplification was:

- resolve the polar pencil on a terminal quartic;
- use adjunction/discrepancy to constrain a generic fibre \(A\);
- for terminal quartics, expect \(A\) to be del Pezzo;
- use
  \[
  e\deg A\le16
  \]
  to reduce to low del Pezzo degree;
- degree 4 and 5 had already been substantially treated;
- a new discrepancy argument was proposed to eliminate planes, quadrics and cubic scrolls because a covering curve would have
  \[
  (K_A+H|_A)\cdot C<0.
  \]

**Important:** that discrepancy argument had not yet been written out or checked. Do not mark it proved.

## Remaining work in B2-L

1. Formalise the terminal-quartic fibre/discrepancy argument.
2. Complete the nonfactorial/singular quartic exceptional-divisor classification.
3. Revisit the deferred general case where \(\dim\operatorname{Sing}F\ge2\) can invalidate the earlier exceptional-divisor degree bound.
4. If B2-L is fully closed, move to B2-Q, the persistent \(2+2\) factor branch.
5. If both B2-L and B2-Q close, formulate a general impossibility theorem for scalar degree-\(\le5\) maps on \(\mathbb F_p^5\).

## Audit warnings

Several corrections occurred during the research:

- the naive quintic norm has explicit monochromatic/symmetric APs;
- simple norm-plus-trace perturbations failed computationally;
- “all singular polar intersections imply vanishing Hessian” is false;
- contracted nonlinear divisors can occur with nonzero Hessian;
- the initial \(dP_5\) degeneracy-locus conjecture \(Z=S\) is false;
- generic/special projection centres for \(dP_5\) behave differently.

Any future proof write-up must preserve these corrections.
