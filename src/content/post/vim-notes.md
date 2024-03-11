---
title: "Vim Notes"
publishDate: "11 March 2024"
description: "Vim notes from the book"
tags: ["vim-notes"]
---

## Vim notes from Practical Vim

If you notice that you have to make the same small change in a handful of
places, you can attempt to compose your changes in such a way that they
can be repeated with the dot command. Recognizing those opportunities takes
practice. But if you develop a habit of making your changes repeatable
wherever possible, then Vim will reward you for it.

## {number}<C-a>
Algo interesante para sumar o restar números enteros a un número existente
es colocarle antes el número entero. Por ejemplo teniendo el cursor en 2 y ejecutando
10<C-a> resulta en 12. Queda mucho mejor a reemplazar de a uno y da más flexibilidad.

También no es necesario tener el cursor posicionado en el número a hacer la operación.
<C-a> buscará el primer digito automáticamente en la línea para hacerlo.

Recordar que el <C-x> resta.

## cW

Este me va a servir muchísimo ahora que aprendí sobre él. Muchas veces quiero borrar algo
incluyendo el símbolo que lo precede por ejemplo: "asd:". Y eso mismo lo puedo lograr con cW.
Sin necesidad de hacer cw y luego x.

## C instead of c$
Esoy acostumbrado a que cuando quiero borrar una porción de texto uso el “c$”
pero ahora descubrí que puedo hacer lo mismo con “C”. Damn, queda mucho mejor
y más rápido porque no tengo que buscar el signo de dolar para hacer lo mismo.
