---
title: "ignore node_modules within telescope"
description: "100-days-of-code"
publishDate: "28 January 2024"
tags: ["100-days-of-code"]
---

## rg and telescope

Bueno hoy encontré lo que necesitaba y que no había sabido aplicar bien.
Y era la manera de ocultar los node_modules de telescope, y la forma es
colocando esa carpeta en el .gitignore porque el ripgrep ignora todo lo que está ahí.

Aquí dejo el link de la issue para alguna futura referencia:

https://github.com/nvim-telescope/telescope.nvim/issues/522
