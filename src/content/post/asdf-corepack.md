---
title: "How to use yarn with asdf-nodejs"
publishDate: "01 October 2024"
description: "Using yarn with corepack and asdf"
tags: ["yarn"]
---

La instalación de yarn recomendada por la página oficial es usar una herramienta
llamada Corepack que viene por defecto al instalar Node.js. <br>
Una vez habilitado corepack, se procede a preparar y activar la ultima versión de yarn,
y como paso importante, al finalizar esto, se le debe hacer reshim a nodejs. Esto
significa que actualiza el entorno de nodejs mismo para poder usar yarn efectivamente.

```bash
corepack enable
corepack prepare yarn@stable --activate
asdf reshim nodejs
yarn --version
```

Referencias:
https://github.com/asdf-vm/asdf-nodejs/issues/342
https://github.com/asdf-vm/asdf-nodejs/pull/349/files
