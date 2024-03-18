---
title: "CORS error"
description: "Cors error solution"
publishDate: "18 March 2024"
tags: ["errors"]
---

> Access to fetch at 'http://localhost:3500/' from origin 'https://www.google.com' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource. If an opaque response serves your needs, set the request's mode to 'no-cors' to fetch the resource with CORS disabled.

- Solucionamos usando la librería de CORS en NPM. Y usandola con express como middleware: app.use(cors());
