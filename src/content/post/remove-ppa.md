---
title: "How to remove PPA repo"
publishDate: "10 October 2024"
description: "How to remove ppa"
tags: ["linux"]
---

## Removing PPA

El motivo para esto es evitar que se actualicen aplicaciones que
ya no tenemos en nuestro sistema pero que al instalarlas, las agregamos a un
PPA en particular.

Hay que tener en cuenta en donde están ubicados los PPA, en primer lugar.

```bash
ls /etc/apt/sources.list.d
```

luego eliminar

```bash
sudo rm -i /etc/apt/sources.list.d/myppa.list
```

Si le colocamos en la instalacion alguna key como trusted, tambien deberiamos
removerla

```bash
# list the trusted keys
sudo apt-key list
# remove the key
sudo apt-key del KEY_ID
```

y hacer un ``sudo apt update``. <br>

Todo lo anterior teniendo en cuenta que el paquete ya esta desinstalado del sistema


