---
layout: post
title: "Post: Fecha futura"
date: 9999-12-31
categories:
  - Post
ref: post-future-date
lang: es
last_modified_at: 2017-03-09T12:45:25-05:00
---

Este post vive en el futuro y tiene fecha {{ page.date | date: "%c" }}. Debería aparecer únicamente cuando Jekyll genere tu proyecto incluyendo la opción `--future`.

```bash
jekyll build --future
```