---
layout: post
title: "Caso Extremo: Listas anidadas y mixtas"
categories:
  - Caso Extremo
tags:
  - contenido
  - css
  - caso extremo
  - listas
  - markup
last_modified_at: 2017-03-09T14:25:52-05:00
---

Las listas anidadas y las listas mixtas son un concepto interesante. Es un caso límite para asegurar que las listas dentro de listas no rompen la numeración de la lista ordenada, y que los estilos de las listas tienen la profundidad necesaria.

## Ordenada -- No ordenada -- Ordenada

1. elemento ordenado
2. elemento ordenado
  * **no ordenado**
  * **no ordenado**
    1. elemento ordenado
    2. elemento ordenado
3. elemento ordenado
4. elemento ordenado

## Ordenada -- No ordenada -- No ordenada

1. elemento ordenado
2. elemento ordenado
  * **no ordenado**
  * **no ordenado**
    * elemento no ordenado
    * elemento no ordenado
3. elemento ordenado
4. elemento ordenado

## No ordenada -- Ordenada -- No ordenada

* elemento no ordenado
* elemento no ordenado
  1. ordenado
  2. ordenado
    * elemento no ordenado
    * elemento no ordenado
* elemento no ordenado
* elemento no ordenado

## No ordenada -- No ordenada -- Ordenada

* elemento no ordenado
* elemento no ordenado
  * no ordenado
  * no ordenado
    1. **elemento ordenado**
    2. **elemento ordenado**
* elemento no ordenado
* elemento no ordenado
