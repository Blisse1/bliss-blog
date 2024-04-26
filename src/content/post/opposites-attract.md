---
title: "Codewars Problems"
description: "Codewars practice"
publishDate: "26 April 2024"
tags: ["codewars-problems"]
---

## Opposites Attract
## Description
Timmy & Sarah think they are in love, but around where they live,
they will only know once they pick a flower each. If one of the flowers has an
even number of petals and the other has an odd number of petals it means they are in love.

Write a function that will take the number of petals of each flower and return true if they are in love and false if they aren't.
## Solution
```js
function lovefunc(flower1, flower2){
  // moment of truth
  // even and odd or odd and even, they in love
  // flower1 even, flower2 odd = true
  // flower1 odd, flower2 even = true
  if(flower1 % 2 !== 0 && flower2 % 2 === 0){
    return true;
  }else if(flower1 % 2 === 0 && flower2 % 2 !== 0){
    return true;
  }else{
    return false;
  }
}
```
## Improved solution based on other solutions
```js
function lovefunc(flower1, flower2){
  return flower1 % 2 !== flower2 % 2;
}
```
## Insight
La solución mejorada que vi en soluciones me gustó. Algo para mejorar
es que tengo que pensar en los casos en donde se cumple la condición primero
y ya luego pensar en refactorizar si vi encontré una solución mejor.
