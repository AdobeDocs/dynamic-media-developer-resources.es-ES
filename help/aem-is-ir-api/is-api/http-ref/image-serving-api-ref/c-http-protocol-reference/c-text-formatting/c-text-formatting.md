---
description: El servicio de imágenes proporciona varias alternativas para procesar texto, accesibles con los comandos text= y textPs=.
seo-description: El servicio de imágenes proporciona varias alternativas para procesar texto, accesibles con los comandos text= y textPs=.
seo-title: Formato de texto
solution: Experience Manager
title: Formato de texto
topic: Scene7 Image Serving - Image Rendering API
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Text formatting{#text-formatting}

El servicio de imágenes proporciona varias alternativas para procesar texto, accesibles con los comandos text= y textPs=.

`textPs=` proporciona un alto nivel de similitud con el texto procesado con Adobe Photoshop e Illustrator. `text=` es razonablemente compatible con el texto procesado con Windows Wordpad.

>[!NOTE]
>
>Además de las diferencias enumeradas en otra parte, `text=` produce diferencias sutiles en el texto procesado cuando se compara con `textPs=`. Por ejemplo, los subrayados no tienen el mismo grosor y la posición y los cursiva sintetizados se representan con un ángulo ligeramente diferente. Si el texto no cabe en el espacio disponible, `text=` puede recortar parcialmente la última línea, mientras que solo `textPs=` representará líneas completas.

Todos los comandos de texto aceptan texto con formato basado en un subconjunto de la especificación RTF (Formato de texto enriquecido). Cada capa de texto puede especificar un comando de texto diferente.

La tabla siguiente lista las funciones clave disponibles para cada comando de texto:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Función</b> </th> 
   <th class="entry"> <b> texto=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Véase también</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Compatible con Adobe Photoshop </p> </td> 
   <td> <p> no </p> </td> 
   <td> <p> limitado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flujo de texto a formas arbitrarias </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flujo de texto a través de rutas arbitrarias </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Ajuste de copia </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> Ajuste de copia <p>, \copyfit, \copyfitlines, \copyfitmaxlines </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Márgenes del cuadro de texto </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>\margl, \margr, \margt, \margb </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Justificación completa del párrafo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>\qj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>justificación de la última línea </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Sangría de párrafo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Todo el texto de mayúsculas y minúsculas </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Colores de servicio de imágenes </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Varios modos de suavizado </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>flujo de texto superior inferior/derecha-izquierda </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compatibilidad con Photofont® </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> Administración de fuentes </td> 
  </tr> 
  <tr> 
   <td> <p>Cambiar el tamaño de la capa automáticamente para ajustar el texto </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compatibilidad con CMYK </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flujo de caracteres de derecha a izquierda </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deshabilitar ajuste de palabras </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Cambiar la escala automática del texto para que se ajuste a la capa (con una resolución variable) </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Las cadenas compatibles con RTF pueden ensamblarse manualmente o dando formato al texto deseado en un editor de texto o procesador de textos capaz de guardar archivos RTF. El archivo RTF se puede abrir en un editor de texto sin formato y el contenido RTF sin procesar del archivo se copiará en la dirección URL de la solicitud.

Algunos procesadores de texto generan archivos bastante grandes, que incluyen preámbulos sustanciales que el servicio de imágenes de Scene7 no utiliza. Se recomienda quitar los elementos RTF no utilizados de la cadena antes de pasar la cadena a los comandos de texto.

La codificación de idioma basada en estándares UTF-8 e ISO se admite en cadenas RTF como alternativa a los mecanismos de codificación de caracteres RTF estándar. Esto permite a las aplicaciones enviar texto que no esté en inglés al servidor sin tener conocimiento de la codificación RTF.

Todos los caracteres no compatibles con HTTP deben eliminarse correctamente si se va a transmitir la cadena mediante http. Solo es necesario que se escape &#39;=&#39;, &#39;&amp;&#39; y &#39;%&#39; si la cadena se incorpora al `catalog::Modifiers` campo de un registro de catálogo de imágenes. Los caracteres de control, incluidos `<CR>`, `<LF>`y `<TAB>` deben eliminarse siempre.

Los motores de texto del servicio de imágenes interpretan un subconjunto de comandos definidos por la Especificación de formato de texto enriquecido (RTF), versión 1.6. Este subconjunto se centra en el formato de fuente/carácter, el formato de párrafo sencillo y la compatibilidad con fuentes y conjuntos de caracteres internacionales. En este momento no se admiten construcciones de formato más avanzadas, como hojas de estilo y tablas.

La familiaridad con la especificación de formato de texto enriquecido (RTF), tal como ha publicado Microsoft, es necesaria al intentar construir cadenas de texto codificadas en RTF manualmente.

* [Gestión de fuentes](r-font-handling.md)
* [Gestión de color](r-color-handling.md)
* [Ajuste de copia](r-copy-fitting.md)
* [Capas de texto](r-text-layers.md)
* [Posición del texto](r-text-positioning.md)
* [Caracteres reservados](r-reserved-characters.md)
* [Palabras clave y comandos RTF admitidos](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Ejemplos de codificación RTF](r-rtf-encoding-examples.md)
