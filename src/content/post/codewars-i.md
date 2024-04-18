---
title: "Codewars - Kata VIII (Day 1)"
description: "Codewars practice"
publishDate: "18 April 2024"
tags: ["codewars-problems"]
---

## Problem I (Multiply)
## Description
This code does not execute properly. Try to figure out why.
## Sample Problem
```js
function multiply(a, b){
  a * b
}
```
## My solution
```js
function multiply(a, b){
  return a * b;
}
```
## Insight
Sin comentarios.

## Problem II (Odd or Even)
## Description
Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.
## Sample Problem
```js
function evenOrOdd(number) {

}
```
## My solution
```js
function evenOrOdd(number) {
  return number % 2 === 0 ? "Even" : "Odd";
}
```
## Insight
Sin comentarios.
## Problem III (Convert a Number to a String!)
## Description
We need a function that can transform a number (integer) into a string.
## Sample Problem
```js
function numberToString(num) {
  // Return a string of the number here!
}
```
## My solution
```js
function numberToString(num) {
  return num.toString();
}
```
## Insight
Sin comentarios.
## Problem IV (Reversed Strings)
## Description
Complete the solution so that it reverses the string passed into it.
## Expected Output
```
'world'  =>  'dlrow'
'word'   =>  'drow'
```
## My solution
```js
function solution(str){
  let orderedStringArr = [];
  let reversedStringArr = [];
  for(const string of str){
    orderedString.push(string);
  }
  while(orderedStringArr.length !== 0){
    for(let string of orderedStringArr){
      if(string === orderedStringArr[orderedStringArr.length - 1]){
        let deletedString = orderedStringArr.pop();
        reversedStringArr.push(deletedString);
      }else{
        continue;
      }
    }
  }
  return reversedString.join("")
}
```
## Other useful solutions from which I learned
Bueno, nada como proponer una solución super verbosa y que la solución sea de una línea.
Sin embargo, no me siento para nada mal. Lo hice presionándome como si no existiera un método para eso.
También se me pasó por alto revisar todos los métodos de Array.prototype. Sí alcancé a mirar
que había un toReversed() pero no un reversed() directamente. Ahí ya lo tengo en cuenta para
otro momento.
## Solución mejorada
```js
function solution(str){
  return str.split("").reverse().join("");
}
```
## Insight
Bueno, esta me tuvo cabezón porque no tenía la menor idea de cómo hacerlo.
La forma en la que abarco las cosas cuando no las sé hacer es por un principio
que tengo muy arraigado. Y ese es el de empezar a construir desde lo más simple.
En este ejercicio llegué a un punto en donde solo quería conseguir que la última letra
al menos poder meterla en una array y que al mismo tiempo se eliminara de la array de la palabra
ordenada. Y ya cuando lo conseguí, solo fue cuestión de pensar que necesitaba encerrar eso
en un loop que lo repitiera para cada última palabra hasta que la array de la palabra original
quedara vacía. Bueno, eso hasta que me di cuenta un método que pasé por alto llamado reverse()
