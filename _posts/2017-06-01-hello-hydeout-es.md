---
layout: post
title: Hola Hydeout
excerpt_separator:  <!--más-->
ref: hello-hydeout
lang: es
---

Hydeout actualiza al tema original [Hyde](https://github.com/poole/hyde)
para [Jekyll](http://jekyllrb.com) 3.x y le añade nuevas funcionalidades.

### Mantenlo sencillo

Siguiendo con el tema original Hyde, Hydeout busca mantener el diseño
ligero sin plugins. El uso de JavaScript se limita únicamente a 
Disqus y Google Analytics (y sólo se incluye si las respectivas variables de configuración 
han sido informadas).

Hydeout hace uso extensivo de Flexbox en sus CSS. Si Flexbox no está disponible,
los CSS se degradan a un layout de una sola columna.

### Personalización

Hydeout reemplaza el funcionamiento de Hyde, basado en clases
mediante el uso de las siguiente variables SASS:

```scss
$sidebar-bg-color: #202020 !default;
$sidebar-sticky: true !default;
$layout-reverse: false !default;
$link-color: #268bd2 !default;
```

Para anular estas variables, podemos crear nuestro propio fichero `assets/css/main.scss`.
Definimos nuestras propias variables, y las importamos al SCSS de Hydeout, de la siguiente manera:

```
---
# Jekyll requiere encabezado para los ficheros SCSS
---

$sidebar-bg-color: #ac4142;
$link-color: #ac4142;
$sidebar-sticky: false;
@import "hydeout";
```

Hecha un vistazo al fichero de [_variables](_sass/hydeout/_variables.scss) para ver
otras variables que pueden ser anuladas.

Es posible también insertar etiquetas personalizadas (e.g. para cargar nuestras propias hojas de estilos) 
definiendo nuestros propios `_includes/custom-head.html` o insertar etiquetas al final
del cuerpo (e.g. para JS personalizado) definiendo nuestro propio
`_includes/custom-foot.html`.

### Nuevas Funcionalidades

* Hydeout también añade una nueva página de etiquetas (accesible desde la barra lateral) y un nuevo
  layout de "categoría" para páginas dedicadas a una determinada categoría.

* Las páginas de categoría son añadidas automáticamente a la barra lateral. Todas las demás páginas
  deben tener `sidebar_link: true` en su cabecera para ser mostradas en la 
  barra lateral.

* Una redirección simple a Google search está disponible. Para utilizar 
  Google Custom Search o Algolia o algo diferente,
  debemos anular `search.html`.

* La integración con Disqus está lista de entrada. Solamente debemos añadir lo siguiente a
  nuestro fichero de configuración:

  ```yaml
  disqus:
    shortname: my-disqus-shortname
  ```

  Si no quieres utilizar Disqus o quieres utilizar otro sistema, deberás anular
  `comments.html`.

* Para soportar la integración con Google Analytics, define una variable `google_analytics` con
  tu ID de propiedad en tu fichero de configuración.

Hay también un montón de ajustes menores por todo el tema.
Espero que encaje con tus necesidades!
