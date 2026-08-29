# Development / research continuity log

Status date: 2026-08-29

## Research objective

Investigate Erdős Problem #160 via the symmetric-pattern subproblem and determine whether the known \(1/4\)-type upper-bound mechanism can be improved to a \(1/5\)-type construction using a scalar map on \(\mathbb F_p^5\).

## Key sequence of ideas

1. Reduced the 4-AP symmetric pattern to two coefficient conditions on the line polynomial of a degree-5 map:
   \[
   c_3=-10c_5,\qquad c_1=9c_5.
   \]

2. Tested the obvious quintic norm \(N_{\mathbb F_{p^5}/\mathbb F_p}\).
   - Found explicit failures.
   - In particular, over \(\mathbb F_7\), a suitable irreducible quintic yields a monochromatic 4-AP under the norm.
   - Conclusion: the naive \(P_5\) replacement is dead.

3. Tested lower-degree trace perturbations computationally.
   - Broad natural families still had many violations.
   - These are evidence only, not proofs.

4. Proved degree \(\le4\) scalar polynomial maps cannot work in dimension 5 via Chevalley–Warning on the odd homogeneous parts.

5. Proved the Branch A theorem:
   \[
   Q_5=\lambda L^5
   \Longrightarrow
   \text{centred ABBA exists}.
   \]
   See \`BRANCH_A.md\`.

6. Entered Branch B: genuinely coupled quintic top form.

7. Derived the geometric complete-intersection viewpoint:
   - first polar \(D_hF\), degree 4;
   - third polar \(D_h^3F\), degree 2;
   - generic geometric integrality implies bad points by Lang–Weil.

8. Split persistent non-integrality into factor types:
   - B2-L: linear + cubic;
   - B2-Q: quadratic + quadratic.

9. Focused on B2-L and progressively eliminated:
   - fixed linear factors;
   - bilinear moving factors;
   - degree-2 exceptional divisors;
   - an extensive degree-3 cubic classification;
   - factorial quartic cases;
   - substantial degree-4/5 del Pezzo fibre cases.

10. Corrected multiple overly strong intermediate claims as counterexamples appeared.

## Most important corrections

### Correction A: singular does not imply vanishing Hessian

There are quintics with nonzero Hessian for which every first polar is singular, e.g. forms with a high-multiplicity point.

Therefore smoothness was replaced by **geometric integrality** as the relevant obstruction.

### Correction B: contracted divisors need not divide \(F\)

A nonlinear divisor can be contracted by the polar map while \(\det\operatorname{Hess}F\not\equiv0\).

This forced a finer exceptional-divisor analysis.

### Correction C: \(dP_5\) projection degeneracy

The conjecture

$$
Z=\{p:\ker D_p\ne0\}=S
$$

was false.

Special off-surface projection centres on five Segre threefolds also produce a kernel.

These special centres were then attacked geometrically using the rank-4 quadric containing the projected \(dP_5\).

## Computation notes

Several exact symbolic computations were used during exploration:

- integrability matrices for hidden-normalization pencils on nonnormal cubic models;
- rank calculations for \(dP_5\) symbolic-square spaces;
- explicit Hessian determinants and minors;
- small-prime searches, especially \(p=7\), for quintic candidates.

These calculations are not currently committed as reproducible scripts. If this research is to be audited, reconstruct and commit the exact scripts used for:

- the \(dP_5\) Pfaffian model;
- the directional-derivative rank computation;
- the nonnormal cubic integrability matrices.

## Current branch tree

- Branch A: \(Q_5=\lambda L^5\)
  - **closed by theorem**.
- Branch B: genuinely coupled quintic top
  - generic case: working geometric exclusion;
  - B2-L:
    - degree 1 exceptional geometry: closed;
    - degree 2: working closed;
    - degree 3: working closed;
    - degree 4: **active**;
  - B2-Q:
    - not yet systematically attacked.

## Exact stop point

The user explicitly ordered the mathematics to stop and the work to be documented.

Immediately before the stop, the active argument was:

> On a terminal quartic exceptional divisor, resolve the polar pencil. A generic fibre \(A\) should satisfy an adjunction/discrepancy condition. Combine this with \(e\deg A\le16\) to limit \(A\) to low-degree del Pezzo/scroll-type surfaces. Planes, quadrics and cubic scrolls were suspected to be excluded because a covering curve would make \(K_A+H|_A\) negative.

This was only a proposed argument. It was **not yet completed**.

## Next action when research resumes

Do **not** continue from memory.

1. Read \`README.md\`, \`BRANCH_A.md\`, this file, and \`B2L_STATUS.md\`.
2. Re-establish the exact hypotheses of the quartic exceptional-divisor branch.
3. Write the terminal-quartic discrepancy/adjunction argument fully.
4. Check whether it really eliminates plane, quadric and cubic-scroll fibres.
5. Only then continue to any residual quartic cases.
