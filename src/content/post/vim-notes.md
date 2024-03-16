---
title: "Vim Notes"
publishDate: "13 March 2024"
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

## gU and gu
guaw para convertir una palabra en minuscula y gUaw para convertirla en mayúscula
Lo mismo para párrafos. gUap para mayus en parrafos y lo mismo para minus.
gUU para mayus en la misma linea.

## gcG
Comenta de una linea hacia abajo

## <C-r>0
Pega contenido del register

## gv
No sé si este pueda ser de utilidad pero igual por alguna razón lo quiero colocar
Este me permite reseleccionar una región previa en la que estuve en visual-mode

## Toggling the free end of a selection
Esta si está re buena. Con la letra o estando en visual-mode y teniendo una
región de texto seleccionado, puedo cambiar la posición del cursor para modificar
a voluntad la región seleccionada

## <C-v> y r
<C-v> para entrar al visual-block mode y r para reemplazar toda esa columna.

## Algo de historia
Vim traces its ancestry back to vi, which is where the modal editing paradigm
was conceived. In turn, vi traces its ancestry back to a line editor called ex,
which is why we have Ex commands. The DNA of these early Unix text editors
is preserved in modern Vim. For some line-oriented tasks, Ex commands are
still the best tool for the job

ed was the original Unix text editor

## Replace
El comando ex que va así: :%s/palabra/reemplazo es muy util cuando uno quiere
cambiar una palabra por otra de manera rápida. Ahorra mucho tiempo y me gusta usarlo.
