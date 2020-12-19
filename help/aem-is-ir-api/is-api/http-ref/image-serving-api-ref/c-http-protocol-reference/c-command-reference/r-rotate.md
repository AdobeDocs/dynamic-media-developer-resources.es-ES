---
description: Rotar imagen. Gira la imagen, el texto o la capa de color sólido según el ángulo especificado.
seo-description: Rotar imagen. Gira la imagen, el texto o la capa de color sólido según el ángulo especificado.
seo-title: rotar
solution: Experience Manager
title: rotar
topic: Scene7 Image Serving - Image Rendering API
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# rotate{#rotate}

Rotar imagen. Gira la imagen, el texto o la capa de color sólido según el ángulo especificado.

`rotate= *`Ángulo`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Ángulo</span> </p> </td> 
  <td class="stentry"> <p>Ángulo de rotación en grados (real). </p></td> 
 </tr> 
</table>

Los ángulos positivos rotan en el sentido de las agujas del reloj. El punto de anclaje de la capa ( `anchor=` o `catalog::Anchor`) sirve como centro de rotación. El rectángulo de capa se amplía y se ajusta alrededor de los datos rotados según sea necesario para evitar el recorte. La rotación se aplica después de rellenar el área de fondo de la capa con `color=`. `bgColor=` se puede utilizar para añadir color de fondo al rectángulo delimitador después de la rotación.

## Propiedades {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Capa. Se aplica a la capa actual o a la capa 0 si `layer=comp`. Omitido por capas de efectos.

## Predeterminado {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, sin rotación.

## Ejemplo {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Coloque una etiqueta &quot;En venta&quot; cerca de la esquina superior izquierda de las imágenes en un catálogo de imágenes. La imagen de la etiqueta ya tiene el tamaño correcto para la vista de 300 x 300 y debe girarse 30 grados a la izquierda. Rellene el cuadro de texto con un color blanco y semiopaco para mejorar la etiqueta.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Aplicamos `size=` a la capa 0 para establecer el tamaño de vista, en lugar de utilizar `wid=` y `hei=`. Esto permite que `myImageId` se cambie el tamaño sin cambiar el tamaño final de `labelImage`. También es necesario especificar `scl=1`; de lo contrario, la imagen compuesta podría escalarse a `attribute::DefaultPix` (a menos que se establezca en 0,0). `color=` agrega el color de fondo semiopaco al cuadro de texto antes de la rotación.

El origen de ambas capas se establece en las esquinas superiores izquierdas para lograr la alineación deseada. Tenga en cuenta que el punto de origen de la capa 1 se aplica a `labelImage`después de haber girado.

Consulte [Ejemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) en [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) para ver un ejemplo de texto rotado.

## Véase también {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
