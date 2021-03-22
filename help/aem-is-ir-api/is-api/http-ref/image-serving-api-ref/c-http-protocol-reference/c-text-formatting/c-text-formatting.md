---
description: Image Serving proporciona varias alternativas para procesar texto, accesibles con los comandos text= y textPs=.
seo-description: Image Serving proporciona varias alternativas para procesar texto, accesibles con los comandos text= y textPs=.
seo-title: Formato del texto
solution: Experience Manager
title: Formato del texto
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 6%

---


# Formato de texto{#text-formatting}

Image Serving proporciona varias alternativas para procesar texto, accesibles con los comandos text= y textPs=.

`textPs=` proporciona un alto nivel de similitud con el texto procesado con Adobe Photoshop y Illustrator. `text=` es razonablemente compatible con el texto procesado con Windows WordPad.

>[!NOTE]
>
>Además de las diferencias enumeradas en otra parte, `text=` produce diferencias sutiles en el texto representado cuando se compara con `textPs=`. Por ejemplo, los subrayados no tienen el mismo grosor y la posición, y la cursiva sintetizada se representa en un ángulo ligeramente diferente. Si el texto no se ajusta al espacio disponible, `text=` puede recortar parcialmente la última línea, mientras que `textPs=` solo procesará líneas completas.

Todos los comandos de texto aceptan texto con formato basado en un subconjunto de la especificación RTF (Formato de texto enriquecido). Cada capa de texto puede especificar un comando de texto diferente.

En la tabla siguiente se enumeran las funciones clave disponibles para cada comando de texto:

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
   <td> <p>Flujo de texto en formas arbitrarias </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flujo de texto por rutas arbitrarias </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Ajuste de copia </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> Ajuste de copia <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Márgenes de cuadros de texto </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Justificación completa del párrafo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
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
   <td> <p>Texto en mayúsculas y minúsculas </p> </td> 
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
   <td> <p>flujo de texto superior inferior/derecho-izquierdo </p> </td> 
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
   <td> <p>Tamaño automático de la capa para ajustar el texto </p> </td> 
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
   <td> <p>Escalar automáticamente el texto para que quepa en la capa (con resolución variable) </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Las cadenas compatibles con RTF se pueden ensamblar manualmente o dando formato al texto deseado en un editor de texto o procesador de texto capaz de guardar archivos RTF. El archivo RTF se puede abrir en un editor de texto sin formato y el contenido RTF sin procesar del archivo se copia en la dirección URL de la solicitud.

Algunos procesadores de texto generan archivos bastante grandes, que incluyen preambles sustanciales que no se utilizan en Dynamic Media Image Serving. Se recomienda quitar los elementos RTF no utilizados de la cadena antes de pasar la cadena a los comandos de texto.

La codificación de idioma basada en los estándares UTF-8 e ISO se admite en cadenas RTF como alternativa a los mecanismos de codificación de caracteres RTF estándar. Esto permite que las aplicaciones envíen texto que no esté en inglés al servidor sin tener conocimiento de la codificación RTF.

Todos los caracteres no compatibles con HTTP deben tener un escape correcto si se va a transmitir la cadena mediante http. Solo es necesario escapar &#39;=&#39;, &#39;&amp;&#39; y &#39;%&#39; si la cadena se incorpora al campo `catalog::Modifiers` de un registro de catálogo de imágenes. Los caracteres de control, incluidos `<CR>`, `<LF>` y `<TAB>`, siempre deben eliminarse.

Los motores de texto de servicio de imágenes interpretan un subconjunto de comandos definidos por la especificación de formato de texto enriquecido (RTF), versión 1.6. Este subconjunto se centra en el formato de fuente/carácter, el formato de párrafo simple y la compatibilidad con fuentes internacionales y conjuntos de caracteres. En este momento no se admiten construcciones de formato más avanzadas, como hojas de estilo y tablas.

La familiaridad con la especificación de formato de texto enriquecido (RTF), tal como publica Microsoft, es necesaria al intentar construir cadenas de texto codificadas RTF manualmente.

* [Administración de fuentes](r-font-handling.md)
* [Gestión de color](r-color-handling.md)
* [Ajuste de copia](r-copy-fitting.md)
* [Capas de texto](r-text-layers.md)
* [Colocación de texto](r-text-positioning.md)
* [Caracteres reservados](r-reserved-characters.md)
* [Comandos y palabras clave RTF admitidos](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Ejemplos de codificación de RTF](r-rtf-encoding-examples.md)
