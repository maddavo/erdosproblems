# Erdős Problem #160 — research notes

Status date: 2026-08-29  
Branch: \`research/160-notes\`

## Problem

Let \(h(N)\) be the least number of colours required to colour \(\{1,\dots,N\}\) so that every 4-term arithmetic progression receives at least three distinct colours.

Equivalently, for every pair of colour classes, their union is 4-AP-free.

The project in this branch investigates the upper-bound side, especially the symmetric two-colour pattern

$$
A\,B\,B\,A.
$$

The working objective is to understand whether the recent \(N^{1/4+o(1)}\)-type construction can be improved toward exponent \(1/5\) by constructing a scalar colour map on \(\mathbb F_p^5\).

## Immediate algebraic target

For a map

$$
Q:\mathbb F_p^5\to\mathbb F_p,
$$

we seek to forbid, for all \(x\) and all nonzero \(h\),

$$
Q(x-3h)=Q(x+3h),\qquad Q(x-h)=Q(x+h).
$$

For a polynomial \(Q\) of degree at most 5, write

$$
Q(x+th)=c_0+c_1t+\cdots+c_5t^5.
$$

The symmetric condition is exactly

$$
c_3=-10c_5,\qquad c_1=9c_5.
$$

For a centred progression this becomes, in homogeneous components,

$$
Q_1(h)=9Q_5(h),\qquad Q_3(h)=-10Q_5(h).
$$

## Main completed result

The cleanest proved result from the current research is the **Branch A impossibility theorem**:

> If \(p>5\), \(\deg Q\le5\), and the homogeneous quintic part is rank one,
> \[
> Q_5=\lambda L^5,
> \]
> then \(Q\) necessarily has a nontrivial centred symmetric 4-AP.

See [BRANCH_A.md](BRANCH_A.md).

This eliminates the entire rank-one quintic-top branch, including arbitrary quadratic and quartic lower-degree terms.

## Branch B

The only degree-\(\le5\) polynomial route left is therefore a genuinely coupled quintic top form

$$
Q_5\ne \lambda L^5.
$$

The research then split according to the geometry of the first-polar / third-polar intersection and, within the persistent-linear-factor case, the exceptional divisors of the polar map.

The working branch tree and all eliminations/corrections are recorded in [B2L_STATUS.md](B2L_STATUS.md).

## Current stopping point

Work was explicitly stopped for documentation while attacking the **degree-4 exceptional-divisor** remainder of B2-L.

At the stop point:

- degree-2 exceptional divisors had been eliminated in the working proof;
- the large degree-3 cubic branch had been reduced case-by-case and treated as eliminated in the working proof;
- factorial quartic exceptional divisors had been treated as eliminated;
- projected degree-4 and degree-5 del Pezzo fibre cases had been substantially reduced;
- the last active direction was the remaining **nonfactorial / sufficiently singular quartic threefold** case, especially low-degree fibre surfaces;
- a proposed discrepancy argument for planes, quadrics and cubic scrolls had **not yet been written out and should not be treated as proved**.

See [DEVELOPMENT.md](DEVELOPMENT.md) for the exact resume point.

## Confidence labels

These notes distinguish three levels:

- **Proved in current work** — a complete algebraic argument was written and checked internally.
- **Working elimination** — a detailed proof sketch exists in the chat, but it has not been independently audited or rewritten publication-style.
- **Computational evidence** — exact or sampled calculations informed the branch but do not substitute for proof.

Before publication or external mathematical claim, every working elimination should be independently checked.

## References

See [REFERENCES.md](REFERENCES.md).
