---
description: Cuantificación de color. Especifica atributos de cuantificación de color para la conversión de salida del GIF.
solution: Experience Manager
title: cuantificar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# cuantificar{#quantize}

Cuantificación de color. Especifica atributos de cuantificación de color para la conversión de salida del GIF.

` quantize= *`type`*[, *`estremecimiento`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> tipo de paleta </p> <p>Seleccionar ' <span class="codeph"> web </span>' o ' <span class="codeph"> mac </span>' para elegir una paleta predefinida o establecer como ' <span class="codeph"> adaptable </span>' para calcular una paleta óptima para la imagen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> estremecimiento </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {difusa|desactivada} </span> opciones de tramado </p> <p>Seleccione "difusa" para la difusión de errores de Floyd-Steinberg o "desactivada" para desactivar el tramado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de colores de salida (entero) incluidos en ' <span class="codeph"> adaptable </span>' paleta. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> debe estar entre 2 y 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Lista separada por comas de colores de RGB forzados en formato hex6. Permite especificar los colores forzados que se van a incluir en un <span class="codeph"> adaptable </span>' paleta. Si el número de colores especificado es menor que <span class="codeph"> numColors </span>Sin embargo, los colores adicionales se calculan en función del contenido de la imagen. </p> <p>Solo se usa si <span class="codeph"> fmt=gif </span> o <span class="codeph"> fmt=gif-alpha </span>. Se ignora en caso contrario. Los colores especificados con <span class="codeph"> <span class="varname"> colorList </span> </span> deben ser valores de RGB en formato hex6 (consulte <span class="codeph"> color </span>); no se permiten otros especificadores de color. </p> </td> 
 </tr> 
</table>

## Predeterminado {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Ejemplo {#section-b3a979dc9ae3459baa093bf17310988f}

Genera una miniatura de GIF utilizando &#39; `web`&#39; y sin tramado:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Convierta la imagen en un GIF bi-tonal con transparencia de key-color y fuerza los colores a blanco y negro:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
