---
description: Cuantificación de color. Especifica atributos de cuantificación de color para la conversión de salida GIF.
seo-description: Cuantificación de color. Especifica atributos de cuantificación de color para la conversión de salida GIF.
seo-title: cuantificar
solution: Experience Manager
title: cuantificar
topic: Scene7 Image Serving - Image Rendering API
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 3%

---


# cuantificar{#quantize}

Cuantificación de color. Especifica atributos de cuantificación de color para la conversión de salida GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptable|web|mac}  </span> </p> <p>Especifica el tipo de paleta. </p> <p>Establezca <span class="codeph"> adaptable </span> para calcular una paleta óptima para la imagen. </p> <p>Establezca <span class="codeph"> web </span> o <span class="codeph"> mac </span> para elegir una paleta predefinida. </p> <p> <p>Nota:  El tipo de pallet <span class="codeph"> mac </span> solo es compatible con los formatos GIF y PNG8, pero no con los formatos GIF-Alpha y PNG8-Alpha. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tramado  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {difusión|desactivado}  </span> </p> <p>Especifica las opciones de tramado. </p> <p>Establecida en <span class="codeph"> difusión </span> para la difusión de errores de Floyd-Steinberg </p> <p>Establezca <span class="codeph"> en </span> para deshabilitar el tramado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>Número de colores de salida (2-256) </p> <p>Especifica cuántos colores se incluyen en la paleta <span class="codeph"> adaptable </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>Lista separada por comas de colores RGB forzados en formato hex6 </p> <p>Permite especificar colores para incluirlos en una paleta <span class="codeph"> adaptable </span>. Si el número de colores especificado es menor que <span class="codeph"> <span class="varname"> numColors </span> </span>, se calculan colores adicionales en función del contenido de la imagen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-8ab5035055b24b858270d260912a7f3d}

Solicitar atributo. Se aplica independientemente de la configuración de la capa actual. Se utiliza solamente si `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` o `fmt=png8-alpha`. Omitido de otro modo.

Los colores especificados con ` *`colorList`*` deben constar de valores RGB en formato hex6 (consulte ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`) sin el prefijo &#39; `0x`&#39;. No se permiten otros especificadores de color. *`numColors`* debe estar entre 2 y 256.

## Predeterminado {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Ejemplo {#section-e34aca7587d548a7ae9d4266b80c9451}

Genere una miniatura GIF con la paleta `web` sin tramado:

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Convierta la imagen en un GIF bitonal con transparencia de color clave y fuerza los colores a blanco y negro:

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Véase también {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
