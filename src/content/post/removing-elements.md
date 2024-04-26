---
title: "Codewars VII (Kata VIII)"
description: "Codewars practice"
publishDate: "23 April 2024"
tags: ["codewars-problems"]
---

## Problem IV (Smallest Integer)
## Description
Given an array of integers your solution should find the smallest integer.
## Expected Output
```
Given [34, 15, 88, 2] your solution will return 2
Given [34, -345, -1, 100] your solution will return -345
```
## My solution
```js
class SmallestIntegerFinder {
  findSmallestInt(args) {
   return args.sort((a, b) => {
     return a - b;
   })[0];
}
}
}
```
## Improved Final Solution based on other people's solutions
```js
class SmallestIntegerFinder {
  findSmallestInt(args) {
    return Math.min(...args)
  }
}
```
## Insight
Con este ejercicio aprendí que hay un método de Math llamado .min() que
retorna el valor menor de una lista de parámetros
