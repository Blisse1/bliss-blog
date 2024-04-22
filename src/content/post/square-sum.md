---
title: "Codewars VI (Kata VIII)"
description: "Codewars practice"
publishDate: "22 April 2024"
tags: ["codewars-problems"]
---

## Problem VI (Square(n) sum)
## Description
Complete the square sum function so that it squares each number passed into it and then sums the results together.
## Final Solution
_(Se me olvidó agregar la primera solución que planteé)_
```js
function squareSum(numbers){
  // "you should use spreading or other copying methods where possible to
  // create new arrays and objects as the accumulator,
  // rather than mutating the existing one." - from developer.mozilla.org
  let numbersCopy = [...numbers]; // like .splice()
  let initialValue = 0;
  return numbersCopy.map(x => x ** 2).reduce((accumulator, currentValue) => {
    return accumulator + currentValue
  }, initialValue);
}
```
## Insight
Aquí por fin hice uso de un .map() y un .reduce(). En donde tenemos que el map
me retorna una array con los valores de la array original modificados por una expresión.
En este caso quería que cada elemento estuviera elevado a la dos. Y luego el reduce()
que en este caso hice que sumara cada valor de la array modificada, colocando un initialValue de 0
para poder pasar el test de una array vacía, con eso me iba a retornar el mismo cero al no
tener valores que sumar y no undefined.
Por último, al estar leyendo acerca del reduce lo que recomiendan desde el MDN y lo que considero
buena práctica es no modificar en lo posible la array que me dan, sino que mejor hacer una copia y trabajar
sobre ella. Más que tratar de buscar una solución concisa y con pocas líneas, también me preocupa sacar
una solución que realmente pueda aplicar en la vida real. Por eso haré lo posible por hacer copias
tanto de Strings como de Arrays y trabajar sobre ellas. Tanto el spread operator en Arrays
como el slice en Strings
