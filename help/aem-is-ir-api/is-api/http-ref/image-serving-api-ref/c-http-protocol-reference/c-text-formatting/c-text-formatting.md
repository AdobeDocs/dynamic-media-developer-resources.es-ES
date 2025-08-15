---
description: El servicio de imágenes proporciona varias alternativas para representar texto, accesibles con los comandos text= y textPs=.
solution: Experience Manager
title: Formato de texto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 6%

---

# Formato de texto{#text-formatting}

El servicio de imágenes proporciona varias alternativas para representar texto, accesibles con los comandos text= y textPs=.

`textPs=` proporciona un alto nivel de similitud con el texto procesado con Adobe Photoshop y Illustrator. `text=` es razonablemente compatible con el texto procesado con Windows Wordpad.

>[!NOTE]
>
>Además de las diferencias enumeradas en otra parte, `text=` produce diferencias sutiles en el texto procesado al compararlo con `textPs=`. Por ejemplo, los subrayados no tienen el mismo grosor y posición, y la cursiva sintetizada se procesa en un ángulo ligeramente diferente. Si el texto no cabe en el espacio disponible, `text=` puede recortar parcialmente la última línea, mientras que `textPs=` solo procesa líneas completas.

Todos los comandos de texto aceptan texto con formato basado en un subconjunto de la especificación RTF (formato de texto enriquecido). Cada capa de texto puede especificar un comando de texto diferente.

En la tabla siguiente se enumeran las funciones clave disponibles para cada comando de texto:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> característica</b> </th> 
   <th class="entry"> <b> texto=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Ver también</b> </th> 
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
   <td> <p>Desplazar texto a formas arbitrarias </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Desplazar texto por rutas arbitrarias </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Copiado </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> Montaje <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Márgenes de cuadro de texto </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Justificación del párrafo completo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>justificación de última línea </p> </td> 
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
   <td> <p>Texto de mayúsculas y minúsculas </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Colores para servicio de imágenes </p> </td> 
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
   <td> <p>flujo de texto de arriba a abajo/derecha a izquierda </p> </td> 
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
   <td> <p>Ajustar automáticamente la capa al texto </p> </td> 
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
   <td> <p>Escalar texto automáticamente para ajustar la capa (con resolución variable) </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Las cadenas compatibles con RTF se pueden ensamblar manualmente o dando formato al texto deseado en un editor de texto o procesador de texto capaz de guardar archivos RTF. El archivo RTF se puede abrir en un editor de texto sin formato y el contenido RTF sin procesar relevante del archivo se copia en la dirección URL de la solicitud.

Algunos procesadores de texto generan archivos bastante grandes, que incluyen preámbulos sustanciales que no se utilizan en el servicio de imágenes de Dynamic Media. Se recomienda eliminar los elementos RTF no utilizados de la cadena antes de pasar la cadena a los comandos de texto.

Las cadenas RTF admiten la codificación de idioma basada en los estándares UTF-8 e ISO como alternativa a los mecanismos de codificación de caracteres RTF estándar. Esto permite a las aplicaciones enviar texto que no esté en inglés al servidor sin tener conocimientos de codificación RTF.

Todos los caracteres no compatibles con HTTP deben escapar correctamente, si la cadena se va a transmitir mediante HTTP. Solo es necesario aplicar secuencias de escape a &#39;=&#39;, &#39;&amp;&#39; y &#39;%&#39; si la cadena se incorpora al campo `catalog::Modifiers` de un registro de catálogo de imágenes. Los caracteres de control, incluidos `<CR>`, `<LF>` y `<TAB>`, siempre se deben quitar.

Los motores de texto del servicio de imágenes interpretan un subconjunto de comandos definidos por la especificación de formato de texto enriquecido (RTF), versión 1.6. Este subconjunto se centra en el formato de fuentes/caracteres, el formato de párrafo sencillo y la compatibilidad con fuentes internacionales y conjuntos de caracteres. En este momento no se admiten construcciones de formato más avanzadas, como hojas de estilo y tablas.

Es necesario estar familiarizado con la especificación de formato de texto enriquecido (RTF), tal como la publica Microsoft, al intentar construir cadenas de texto con codificación RTF manualmente.

* [Administración de fuentes](r-font-handling.md)
* [Gestión de color](r-color-handling.md)
* [Copiado](r-copy-fitting.md)
* [Capas de texto](r-text-layers.md)
* [Posición del texto](r-text-positioning.md)
* [Caracteres reservados](r-reserved-characters.md)
* [Palabras clave y comandos RTF admitidos](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Ejemplos de codificación RTF](r-rtf-encoding-examples.md)
