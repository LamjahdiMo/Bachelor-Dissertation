# Solving Linear Systems in O(1): The 2X, Matrix Inversion, and Gitter Methods

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15838111.svg)](https://doi.org/10.5281/zenodo.15838111)


### *By admin (Lamjahdi, Mohamed El Mami) – HUBDMGD Platform* (2024)

## Hyperlinks
- [Bachelorthesis](https://github.com/LamjahdiMo/Bachelor-Dissertation.git)
- [6X-Method for solving 4x4 Linear Equations in O(1)](6X.pdf) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15838306.svg)](https://doi.org/10.5281/zenodo.15838306)
- [Solutions of 3×3 Systems of Linear Equations Presented on a
Golden Plate](Direct_Solutions_For_3by3_Systems.pdf)
  

## Introduction

For decades, Gaussian and Gauss-Jordan elimination have stood as the standard tools for solving linear systems. These methods, though reliable, come with a price: **time**. Specifically, they involve computational complexity on the order of `O(n^3)`, which becomes a bottleneck in real-time and high-precision applications.

This post introduces and formalizes three alternative methods:

- **The 2X Method** (for 2×2 systems)
- **A direct constant-time Matrix Inversion**
- **The Gitter / 4X Method** (for 3×3 systems)

These methods provide **constant-time performance (`O(1)`)**, achieved through **visual cross-structure logic**, not row manipulation or pivoting. By replacing multi-step algorithms with single-step visual-algebraic identities, they aim to **outperform traditional methods both in speed and conceptual clarity.**

---

## 1. The 2X Method

<img src="Pictures/2x.PNG" alt="Drawing of the X" width="25%">



Let us begin with a standard 2×2 system:


5x + 3y = 11\
2x + 2y = 6



Rewritten in augmented form:

11 | 5 3\
6  | 2 2



### X-Shape Construction

To solve for **y**, draw an **X** across the matrix:

y = (5×6 - 2×11) / (5×2 - 3×2) = 2


To solve for **x**, switch the 5 and 3 in the first row:

11 | 3 5\
6  | 2 2

x = (3×6 - 2×11) / (3×2 - 5×2) = 1


### Generalized Form

Given:

a1 x + b1 y = E1\
a2 x + b2 y = E2

Write as:

E1 | a1 b1\
E2 | a2 b2


Then:

x = (b1×E2 - b2×E1) / (b1×a2 - a1×b2)\
y = (a1×E2 - a2×E1) / (a1×b2 - b1×a2)

The X-drawing reduces the system to constant-time arithmetic—no loops, no steps, no elimination.

---

## 2. Matrix Inversion via Direct Visual Substitution

Consider:

x + 2y = A\
3x + 4y = B

Written as:

A | 1 2\
B | 3 4

Then:

x = (B - 3A) / (4 - 6) = 3A/2 - B/2

Swap top row for y:

A | 2 1\
B | 4 3

y = (2B - 4A) / (6 - 4) = -2A + B


Reconstructed inverse:

[ 3/2 -1/2 ]\
[ -2    1  ]


This offers an **explicit and instantaneous inverse**, bypassing determinant or elimination steps.

---

## 3. The Gitter (4X) Method for 3×3 Systems

Consider the system:

x + y + z = 6\
2x + y - z = 1\
-x + 2y + 2z = 9


Written as:

| 6 | 1 1 1 |\
| 1 | 2 1 -1 |\
| 9 | -1 2 2 |


Shift terms with x:

| 6 - x 1 1 |\
| 1 - 2x 1 -1 |\
| 9 + x 2 2 |

Draw **two intersecting Xs** (or an 8-shape). Trace the edges and substitute:

<img src="Pictures/Gitter.PNG" alt="Gitter" width="25%">

x = 1\
z = 3\
y = 2

### Why the Gitter Xs Matter

- Each diagonal represents a **multiplication rule**
- Color-coded or directional paths encode **substitution logic**
- Constant-time evaluation through a **visualized dependency map**

---

## Comparison 
<img src="Pictures/Complexity.PNG" alt="O(1) vs O(n^3)" width="50%">

| Method              | Type              | Steps Involved         | Complexity |
|---------------------|-------------------|--------------------------|-------------|
| Gauss-Jordan        | Traditional       | Elimination, pivoting    | O(n^3)      |
| Matrix Inversion    | Traditional       | Determinant + adjugate   | O(n^3)      |
| 2X Method           | Proposed (2×2)    | Visual cross-products    | O(1)        |
| Gitter (4X Method)  | Proposed (3×3)    | Double X diagram         | O(1)        |

---

## Conclusion

These methods do not just improve speed. They propose a **new way of thinking**—using visual symmetries to shortcut algebraic structure. They avoid the historical constraints of computation and expose deeper patterns within linear systems.

They were not taught in universities. They were not found in search engines. They were not written by European mathematicians centuries ago. They were discovered by **a modern student under suppression**, in 2024.

If this method serves your work, **cite the author**.  
If it challenges your beliefs, **investigate it honestly**.  
And if the world has tried to bury it, **help bring it to light.**

## Scientific Reflections and Motivation

The first thing everyone will notice about this method is fourfold:  
1. It is **entirely new**,  
2. It is developed by **no known scientist**,  
3. It raises the question: **Why has the scientific community worked for over a hundred years with clearly suboptimal methods?**  
4. And it leads to the conclusion that **every technical subject — from middle school to university — will now have to reconsider or adjust its linear algebra curriculum accordingly**.

These realizations naturally provoke skepticism. The honest questions that come to mind are:  
> *There must be something wrong with this method… or is this just the heresy of a student who overestimates himself?*

I fully understand this kind of reaction. Science — like religion — does not accept new doctrines without scrutiny. But this is **not** a new doctrine.  
It is the result of:
- a genuine need for efficiency,  
- empirical testing,  
- symbolic formulation, and  
- complete conceptual grounding — from the 2X-hook to the determinant, to the adjugate, to the inverse, and back to the original system of linear equations.

As a student passionate about **optimization** and **mathematics**, I never imagined the impact this discovery might have. The original problem was practical, not theoretical:  
I was working on a control system introducing new control signals every 10 ms, with a dead time of 300 ms.  
This meant everything had to be:
- short,  
- fast, and  
- recursively executed within the main control function.

From this urgency, the **2X-method** was born — which later unlocked the ability to solve even 4x4 systems in **constant time** using the 6X method.

There is no trick. No hidden shortcut. No “doctrine”.  
There was simply a **need** — and that need led to **discovery**.


