+++
title = "An implementation of the Todd-Coxeter algorithm in python3"
date = "2021-07-11"
author = "j. d. mitchell"
+++

This page is a companion to the paper [The Todd-Coxeter Algorithm for
Semigroups and Monoids]() by T. D. H. Coleman,  [J. D. Mitchell](jdbm.me), [F.
L. Smith](https://flsmith.github.io/), and [M.
Tsalakou](https://mariatsalakou.github.io/). On this page we give an
implementation of the two strategies for congruence enumeration described in
[the paper]() in python3.  The code on this page is expository, and should
probably not be used for anything serious. There are many optimization that
could be applied, but we opted not to do these in order to keep the code short.
Many best practices for software development, such as argument checks,
assertions, docstrings or exceptions, are also absent, please forgive us in
advance.  The C++ library [libsemigroups](https://libsemigroups.readthedocs.io/en/latest/) contains optimized versions of the
code on this page, and we recommend you use this instead!

The essential purpose of the Todd-Coxeter Algorithm is to
compute the action of a finitely presented semigroup or monoid on the
equivalence classes of a left, right, or two-sided congruence. However, again
for the purposes of exposition, we will concentrate on the problem of computing
  the size of a semigroup defined by a finite presentation.

  <!-- TODO add some details about presentations etc --> 

There are two main strategies for Todd-Coxeter: *Felsch* and *HLT*. These are
implemented in the following class `ToddCoxeter`:

{{< gist james-d-mitchell 6b06bc78e2bcdb6dfef53a2654d9f953 >}}

