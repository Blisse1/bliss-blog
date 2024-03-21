---
title: "POST request using curl"
publishDate: "21 March 2024"
description: "Example of sending a post request using curl"
tags: ["curl"]
---

# Example of a POST request using curl
## Posting JSON data
curl -H "Content-Type: application/json" \
-d '{"data": "info"}' \
-X POST \
http://localhost:<port>

