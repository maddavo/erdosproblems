# Branch A impossibility theorem

## Statement

Let \(p>5\) be prime and

$$
Q:\mathbb F_p^5\to\mathbb F_p
$$

be a polynomial of degree at most \(5\). Write

$$
Q=Q_0+Q_1+Q_2+Q_3+Q_4+Q_5
$$

into homogeneous components.

Assume

$$
Q_5=\lambda L^5
$$

for a linear form \(L\) and \(\lambda\in\mathbb F_p\).

Then \(Q\) has a nonzero \(h\) such that

$$
Q(-3h)=Q(3h),\qquad Q(-h)=Q(h).
$$

Thus the four-term progression

$$
-3h,-h,h,3h
$$

has the forbidden symmetric colour pattern.

## Centred reduction

Even homogeneous components cancel automatically under \(h\mapsto-h\).

Put

$$
a=Q_1(h),\qquad b=Q_3(h),\qquad c=Q_5(h).
$$

The two symmetric equalities are

$$
a+b+c=0
$$

and

$$
3a+27b+243c=0.
$$

For \(p>5\), these are equivalent to

$$
b=-10c,\qquad a=9c.
$$

Therefore it suffices to find \(h\ne0\) satisfying

$$
Q_1(h)=9Q_5(h),\qquad Q_3(h)=-10Q_5(h).
$$

## Case 1: \(\lambda=0\)

Then \(Q_5=0\), so we need

$$
Q_1(h)=Q_3(h)=0.
$$

These are homogeneous equations of total degree sum

$$
1+3=4<5
$$

in five variables.

By Chevalley–Warning there is a nonzero common solution.

## Case 2: \(\lambda\ne0\)

Let

$$
H=\ker L.
$$

If there is already \(0\ne z\in H\) with

$$
Q_1(z)=Q_3(z)=0,
$$

we are done because \(Q_5(z)=0\).

So assume no such \(z\) exists.

### Step 1: \(Q_1|_H\ne0\)

If \(Q_1|_H=0\), then \(Q_3|_H\) is a cubic in four variables. Chevalley–Warning gives a nonzero zero, contradiction.

Thus

$$
\ell:=Q_1|_H\ne0.
$$

Set

$$
K=\ker\ell\subset H.
$$

Then \(\dim K=3\).

### Step 2: the cubic on \(K\) is anisotropic

Let

$$
C=Q_3|_K.
$$

If \(0\ne k\in K\) and \(C(k)=0\), then

$$
L(k)=Q_1(k)=Q_3(k)=0,
$$

again giving a bad direction.

Therefore

$$
C(k)=0\Longrightarrow k=0.
$$

So \(C\) is an anisotropic ternary cubic.

### Step 3: surjectivity lemma

Let \(P:\mathbb F_p^3\to\mathbb F_p\) be any degree-\(\le3\) polynomial whose homogeneous cubic part is the anisotropic cubic \(C\).

Then \(P\) is surjective.

For any \(r\in\mathbb F_p\), homogenise \(P(k)-r\) to a homogeneous cubic in four variables \((k,t)\). Chevalley–Warning yields a nonzero zero. It cannot have \(t=0\), because then \(C(k)=0\) would force \(k=0\). Hence \(t\ne0\), and scaling gives \(P(k/t)=r\).

### Step 4: construct \(h\)

Choose \(e\) with \(L(e)=1\), and choose any \(y\ne0\).

Seek

$$
h=ye+z,\qquad z\in H.
$$

Then

$$
Q_5(h)=\lambda y^5.
$$

First impose

$$
Q_1(h)=9\lambda y^5.
$$

Since \(Q_1\) is linear and \(\ell:H\to\mathbb F_p\) is surjective, choose one solution \(z_0\in H\).

All such solutions are

$$
z=z_0+k,\qquad k\in K.
$$

Now consider

$$
P(k)=Q_3(ye+z_0+k).
$$

As a polynomial in \(k\in K\cong\mathbb F_p^3\), it has degree at most 3 and homogeneous cubic part \(C(k)\).

By the surjectivity lemma, choose \(k\) so that

$$
P(k)=-10\lambda y^5.
$$

Then the resulting nonzero \(h\) satisfies

$$
Q_1(h)=9Q_5(h),\qquad Q_3(h)=-10Q_5(h).
$$

Therefore the centred symmetric 4-AP exists.

## Consequence

No scalar degree-\(\le5\) colour map on \(\mathbb F_p^5\) with rank-one quintic top form can provide the desired \(p^5\) construction.

In particular, arbitrary \(Q_2\) and \(Q_4\) do not help: they cancel completely in the centred witness.

## Status

**Proved in current work.**

This is the most mature theorem in the project and should be the first result rewritten publication-style.
