# Using an IDE

### For this lesson, we are going to discuss the Big O notation. Additionally, we will be going over pseudo-code and techniques used to help learn how to logically write code.


## Objectives

**During this topic the student will have a fundemental understanding on IDE setup and use to include the following.**
* **Big O Notation concepts**
* **Logarithms**
* **O(Log N)**

---

## Big O Notation

The Big O notation is used in Computer Science to describe the performance or complexity of an algorithm.
Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.

---

## Introduction

One of the best methods for understanding Big O thoroughly is through code examples.  So, to help you to understand it best; we have provided some common orders of growth along with descriptions and examples when possible.

---

## O(1)

O(1) describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

![](/assets/big_O_01.png)

---

## O(N)

O(N) describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set.  The example below also demonstrates how Big O favours the workst-case performance scenarios; a matching string could be found during any iteration of the ***for loop*** and the function would return early, but Big O notation will always assume the upper limit where the algorithm will perform the maximum number of iterations.

![](/assets/big_O_02.png)

---

## O(N2)

O(N2) represents an algorithm whose performance is directly proportional to the square of the size of the input data set.  