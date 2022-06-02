---
title: cuantificar
description: Cuantificación de color. Especifica atributos de cuantización de color para la conversión de salida del GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# cuantificar{#quantize}

Cuantificación de color. Especifica atributos de cuantización de color para la conversión de salida del GIF.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptable|web|mac} </span> </p> <p>Especifica el tipo de paleta. </p> <p>Establecer como <span class="codeph"> adaptable </span> para calcular una paleta óptima para la imagen. </p> <p>Establecer como <span class="codeph"> web </span> o <span class="codeph"> mac </span> para elegir una paleta predefinida. </p> <p> <p>Nota: La variable <span class="codeph"> mac </span> el tipo de pallet solo es compatible con los formatos GIF y PNG8, pero no con los formatos GIF-alfa y PNG8-Alpha. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {difusión|off} </span> </p> <p>Especifica las opciones de vaciado. </p> <p>Establecer como <span class="codeph"> difuso </span> para la difusión de errores de Floyd-Steinberg </p> <p>Establecer como <span class="codeph"> off </span> para desactivar el vaciado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>Número de colores de salida (2-256) </p> <p>Especifica cuántos colores se incluyen en la variable <span class="codeph"> adaptable </span> paleta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>Una lista separada por comas de colores de RGB forzados en formato hex6 </p> <p>Permite especificar colores para incluirlos en una <span class="codeph"> adaptable </span> paleta. Si el número de colores especificado es menor que <span class="codeph"> <span class="varname"> numColors </span> </span>, los colores adicionales se calculan en función del contenido de la imagen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-8ab5035055b24b858270d260912a7f3d}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Solo se usa si `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`o `fmt=png8-alpha`. En caso contrario, se ignorará.

Los colores especificados con *`colorList`* debe estar formado por valores RGB en formato hex6 (consulte [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) without `0x` prefijo . No se permiten otros especificadores de color. *`numColors`* debe estar entre 2 y 256.

## Predeterminado {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Ejemplo {#section-e34aca7587d548a7ae9d4266b80c9451}

Genere una miniatura de GIF utilizando la variable `web` paleta y sin tramado:

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Convierta la imagen en un GIF bitonal con transparencia de color clave y fuerce los colores a blanco y negro:

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Véase también {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
