---
title: "Node-notes"
publishDate: "17 March 2024"
description: "Node notes"
tags: ["notes"]
---

## express public middleware
Recuerdo haber tenido problemas con este paso cuando hacía un MVC el año pasado.
Ahora que estoy siguiendo y realmente entendiendo, me queda mucho más claro.
En el dir public están las carpetas de css e imagenes, por colocar un ejemplo
Cuando estoy creando las vistas en el dir views los path para el css e imagenes
tienen que ser apuntando solo a las carpetas porque el middleware ya se encarga
de definir una carpeta en donde va a estar el contenido estático
Por lo tanto, si tengo un dir dentro de public con un dir de css, puedo acceder a él
sin problemas desde una view solamente colocando el path de la carpeta y el nombre del archivo
como si estuvieran en root, pero esta vez se comporta estando desde public

## consideraciones
Realmente me parece fascinante entender cómo funcionan bien las cosas. No sabía
que ya estaba utilizando middleware en mi anterior proyecto. Y entender bien la funcionalidad
me parece increíble. Me parece obvio que uno se va a topar con muchas cosas que no sabe,
pero sigo defendiendo que uno las puede abordar mucho mejor si tiene fundamentales solidos.
Tutorial, proyecto guiado _(preferiblemente del mismo tutorial y de una persona con exp)_, y docs.
O docs, tutorial, proyecto.
