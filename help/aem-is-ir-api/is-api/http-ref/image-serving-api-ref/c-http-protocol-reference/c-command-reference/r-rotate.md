---
title: rotar
description: Rotar imagen. Gira la capa de color sólido, de texto o de imagen según el ángulo especificado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---

# rotar{#rotate}

Rotar imagen. Gira la capa de color sólido, de texto o de imagen según el ángulo especificado.

`rotate= *`ángulo`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ángulo</span> </p> </td> 
  <td class="stentry"> <p>Ángulo de rotación en grados (real). </p></td> 
 </tr> 
</table>

Los ángulos positivos giran en sentido horario. El punto de anclaje de capa (`anchor=` o `catalog::Anchor`) sirve como centro de rotación. El rectángulo de capa se amplía y se ajusta alrededor de los datos girados según sea necesario para evitar el recorte. La rotación se aplica después de rellenar el área de fondo de la capa con `color=`. El modificador `bgColor=` se puede usar para agregar color de fondo al rectángulo delimitador después de la rotación.

## Propiedades {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Capa, comando. Se aplica a la capa actual o a la capa 0 si `layer=comp`. Ignorado por las capas de efecto.

## Predeterminado {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, sin rotación.

## Ejemplo {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Coloque una etiqueta &quot;En venta&quot; cerca de la esquina superior izquierda de las imágenes de un catálogo de imágenes. La imagen de la etiqueta ya tiene el tamaño correcto para la vista de 300x300 y debe girarse 30° a la izquierda. Para mejorar la etiqueta, rellene el cuadro de texto con un color blanco y semiopaco.

`http:// *`servidor`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Aplique `size=` a la capa 0 para establecer el tamaño de la vista, en lugar de utilizar `wid=` y `hei=`. Este método permite cambiar el tamaño de `myImageId` sin cambiar el tamaño final de `labelImage`. Especifique también `scl=1`; de lo contrario, la imagen compuesta podría escalarse a `attribute::DefaultPix` (a menos que se establezca en 0,0). El modificador `color=` agrega el color de fondo semiopaco al cuadro de texto antes de la rotación.

El origen de ambas capas se define en la esquina superior izquierda para lograr la alineación deseada. El punto de origen de la capa 1 se aplica a `labelImage` después de girarlo.

Vea [Ejemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) en [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) para ver un ejemplo de texto girado.

## Véase también {#section-c371ee0845994b7382c02e782d1bc595}

[anclaje=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
