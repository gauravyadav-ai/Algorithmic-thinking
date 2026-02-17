# How Algorithms Think → How Neural Networks Learn

This repository is my training ground for understanding learning systems.

Instead of collecting coding solutions, I document the reasoning patterns behind problems and connect them to ideas used in deep learning — memory, representation, optimization behavior, and information flow.

The goal is simple:
build intuition, not memorization.

---

## Motivation

Deep learning models succeed when the structure of the problem is understood correctly.
Architectures alone rarely solve problems — correct assumptions do.

Coding problems act as controlled environments where structure is visible:
constraints, state transitions, search spaces, and invariants.

Real-world ML systems hide the same structure inside data.

This repo is practice for recognizing that structure.

---

## Mental Models Practiced

| Algorithmic Idea          | Neural Network Analogy   |
| ------------------------- | ------------------------ |
| Dynamic Programming state | latent representation    |
| Sliding window constraint | attention context        |
| Graph traversal           | message passing          |
| Greedy choice             | gradient descent step    |
| Memoization               | feature / KV caching     |
| Binary search             | searching loss landscape |

---

## Patterns Covered

* Sliding Window — maintaining dynamic constraints
* Binary Search — exploiting monotonic behavior
* Dynamic Programming — modeling state dependencies
* Graph Traversal — reasoning over structured data
* Greedy — local vs global optimality
* Backtracking — exploring hypothesis space
* Bit Manipulation — compact state encoding

---

## What Each Problem Contains

Each write-up focuses on reasoning rather than code:

* why the naive solution fails
* invariant that makes the solution correct
* complexity justification
* transferable insight

---

## Approach to New Problems

1. Identify constraints
2. Identify stored information (state)
3. Check monotonic behavior
4. Determine dependency structure
5. Choose pattern
6. Optimize

---

## What This Demonstrates

This repository reflects:

* structured thinking
* abstraction ability
* understanding of optimization behavior
* preparation for designing learning systems

---

## Long-Term Goal

To understand learning systems the same way we understand algorithms —
by reasoning about structure, not just running experiments.
