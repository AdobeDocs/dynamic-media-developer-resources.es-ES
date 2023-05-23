---
description: Rotar imagen. Gira la capa de color sólido, de texto o de imagen según el ángulo especificado.
solution: Experience Manager
title: rotar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 2%

---

# rotar{#rotate}

Rotar imagen. Gira la capa de color sólido, de texto o de imagen según el ángulo especificado.

`rotate= *`Ángulo`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Ángulo</span> </p> </td> 
  <td class="stentry"> <p>Ángulo de rotación en grados (real). </p></td> 
 </tr> 
</table>

Los ángulos positivos giran en sentido horario. El punto de anclaje de capa ( `anchor=` o `catalog::Anchor`) sirve como centro de rotación. El rectángulo de capa se amplía y se ajusta alrededor de los datos girados según sea necesario para evitar el recorte. La rotación se aplica después de rellenar el área de fondo de la capa con `color=`. `bgColor=` se puede utilizar para añadir color de fondo al rectángulo delimitador después de la rotación.

## Propiedades {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Capa, comando. Se aplica a la capa actual o a la capa 0 si `layer=comp`. Ignorado por las capas de efecto.

## Predeterminado {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, sin rotación.

## Ejemplo {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Coloque una etiqueta &quot;En venta&quot; cerca de la esquina superior izquierda de las imágenes de un catálogo de imágenes. La imagen de la etiqueta ya tiene el tamaño correcto para la vista de 300x300 y debe girarse 30 grados a la izquierda. Rellene el cuadro de texto con un color blanco y semiopaco para mejorar la etiqueta.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Nosotros aplicamos `size=` a la capa 0 para establecer el tamaño de la vista, en lugar de utilizar `wid=` y `hei=`. Esto permite `myImageId` se redimensionará sin cambiar el tamaño final de `labelImage`. También tenemos que especificar `scl=1`, de lo contrario, la imagen compuesta podría escalarse a `attribute::DefaultPix` (a menos que esté ajustado en 0,0). `color=` agrega el color de fondo semiopaco al cuadro de texto antes de la rotación.

El origen de ambas capas se establece en las esquinas superiores izquierdas para lograr la alineación deseada. Observe que el punto de origen de la capa 1 se aplica a `labelImage`después de haberla girado.

Consulte [Ejemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) para ver un ejemplo de texto girado.

## Véase también {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
