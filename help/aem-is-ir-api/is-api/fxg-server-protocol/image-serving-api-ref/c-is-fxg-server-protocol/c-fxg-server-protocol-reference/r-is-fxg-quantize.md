---
description: Cuantificación de color. Especifica atributos de cuantificación de color para la conversión de salida GIF.
seo-description: Cuantificación de color. Especifica atributos de cuantificación de color para la conversión de salida GIF.
seo-title: cuantificar
solution: Experience Manager
title: cuantificar
topic: Scene7 Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# cuantificar{#quantize}

Cuantificación de color. Especifica atributos de cuantificación de color para la conversión de salida GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Tipo de  </span> paleta {adaptable|web|mac} </p> <p>Seleccione ' <span class="codeph"> web </span>' o ' <span class="codeph"> mac </span>' para elegir una paleta predefinida o establezca en ' <span class="codeph"> adaptable </span>' para calcular una paleta óptima para la imagen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> tramado  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Opciones de  </span> tramado de {difusión|apagado} </p> <p>Seleccione 'difuso' para la difusión de errores de Floyd-Steinberg o 'desactivado' para desactivar el tramado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de colores de salida (entero) incluidos en la paleta ' <span class="codeph"> adaptable </span>'. </p> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> debe estar entre 2 y 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>Lista separada por comas de colores RGB forzados en formato hex6. Permite especificar colores forzados para incluirlos en una paleta adaptable <span class="codeph"> ' </span>'. Si el número de colores especificado es menor que <span class="codeph"> numColors </span>, los colores adicionales se calculan en función del contenido de la imagen. </p> <p>Solo se utiliza si <span class="codeph"> fmt=gif </span> o <span class="codeph"> fmt=gif-alpha </span>. Omitido de otro modo. Los colores especificados con <span class="codeph"> <span class="varname"> colorList </span> </span> deben ser valores RGB en formato hex6 (consulte <span class="codeph"> color </span>); no se permiten otros especificadores de color. </p> </td> 
 </tr> 
</table>

## Predeterminado {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Ejemplo {#section-b3a979dc9ae3459baa093bf17310988f}

Genere una miniatura GIF con la paleta &#39; `web`&#39; y sin tramado:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Convierta la imagen en un GIF bitonal con transparencia de color clave y fuerza los colores a blanco y negro:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
