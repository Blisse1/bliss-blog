---
title: "Codewars V (Kata VIII)"
description: "Codewars practice"
publishDate: "22 April 2024"
tags: ["codewars-problems"]
---

## Problem V (Remove Characters)
## Description
It's pretty straightforward. Your goal is to create a function that removes the first and last characters of a string. You're given one parameter, the original string. You don't have to worry about strings with less than two characters.
## Solution
```js
function removeChar(str){
  return str.slice(1, str.length - 1);
};
```
## Improved Final Solution based on other solutions
```js
function removeChar(str){
  return str.slice(1, -1);
};
```
## Insight
El método de Strings llamado .slice() vino bien aquí. Una cosa a mejorar
es que hay que tener en cuenta que el segundo parámetro de slice hace referencia
directamente al index de la string. Por lo tanto, colocar solamente -1 ya hace
referencia al último elemento de la string que no quiero que se incluya
y así obviar el hecho de colocar str.length - 1.
