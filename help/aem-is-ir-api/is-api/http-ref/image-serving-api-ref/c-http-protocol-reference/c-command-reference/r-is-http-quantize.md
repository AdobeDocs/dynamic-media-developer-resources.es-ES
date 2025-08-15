---
title: cuantificar
description: Cuantificación de color. Especifica atributos de cuantificación de color para la conversión de salida de GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# cuantificar{#quantize}

Cuantificación de color. Especifica atributos de cuantificación de color para la conversión de salida de GIF.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tipo </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Especifica el tipo de paleta. </p> <p>Establezca en <span class="codeph"> </span> adaptable para calcular una paleta óptima para la imagen. </p> <p>Establezca <span class="codeph"> web </span> o <span class="codeph"> mac </span> para elegir una paleta predefinida. </p> <p> <p>Nota: El tipo de pallet <span class="codeph"> mac </span> solo es compatible con los formatos GIF y PNG8, pero no con los formatos GIF-Alpha y PNG8-Alpha.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tramado </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {difusa|desactivada} </span> </p> <p>Especifica las opciones de tramado. </p> <p>Se estableció en <span class="codeph"> difuso </span> para la difusión de error de Floyd-Steinberg </p> <p>Se estableció en <span class="codeph"> de </span> para deshabilitar el tramado.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>Número de colores de salida (2-256) </p> <p>Especifica cuántos colores se incluyen en la paleta <span class="codeph"> </span> adaptable.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> lista de colores </span> </span> </p> </td> 
   <td colname="col2"> <p>Lista separada por comas de los colores RGB forzados en formato hex6 </p> <p>Permite especificar los colores que se incluirán en una paleta <span class="codeph"> </span> adaptable. Si el número de colores especificado es menor que <span class="codeph"> <span class="varname"> numColors </span> </span>, se calculan colores adicionales basados en el contenido de la imagen.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-8ab5035055b24b858270d260912a7f3d}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Solo se usa si `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` o `fmt=png8-alpha`. Se ignora en caso contrario.

Los colores especificados con *`colorList`* deben constar de valores RGB en formato hex6 (vea [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) sin prefijo `0x`. No se permiten otros especificadores de color. El modificador *`numColors`* debe ser 2-256.

## Predeterminado {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Ejemplo {#section-e34aca7587d548a7ae9d4266b80c9451}

Genere una miniatura de GIF con la paleta `web` y sin tramado:

`http:// *`*Servidor*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Convierta la imagen en un GIF bitono con transparencia de clave de color. Y, fuerza los colores a blanco y negro:

`http:// *`*Servidor*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Véase también {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
