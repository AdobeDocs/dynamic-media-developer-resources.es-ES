---
description: Uso de la máscara de imagen. Especifica cómo se utiliza la máscara o el canal alfa de la imagen para operaciones en la imagen (por ejemplo, colorize=). Cuando se especifica en una capa de efecto, permite aplicar el efecto al área de fondo de la capa principal o a todo el rectángulo de la capa principal.
seo-description: Uso de la máscara de imagen. Especifica cómo se utiliza la máscara o el canal alfa de la imagen para operaciones en la imagen (por ejemplo, colorize=). Cuando se especifica en una capa de efecto, permite aplicar el efecto al área de fondo de la capa principal o a todo el rectángulo de la capa principal.
seo-title: maskUse
solution: Experience Manager
title: maskUse
topic: Scene7 Image Serving - Image Rendering API
uuid: 2c70da87-f869-495a-be50-226a4516e002
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---


# maskUse{#maskuse}

Uso de la máscara de imagen. Especifica cómo se utiliza la máscara o el canal alfa de la imagen para operaciones en la imagen (por ejemplo, colorize=). Cuando se especifica en una capa de efecto, permite aplicar el efecto al área de fondo de la capa principal o a todo el rectángulo de la capa principal.

`maskUse=norm|invert|off`

La siguiente tabla ilustra el efecto de `maskUse=` en función de la disponibilidad y el tipo de máscara (canal alfa) asociada a la imagen de capa.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valor</b> </th> 
   <th class="entry"> <b> Sin máscara</b> </th> 
   <th class="entry"> <b> Alfa no asociado (o imagen de máscara independiente)</b> </th> 
   <th class="entry"> <b> Alfa asociado (premultiplicado)</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> apagado </span> </p> </td> 
   <td> <p> Rectángulo de imagen opaco </p> </td> 
   <td> <p> Rectángulo de imagen opaco </p> </td> 
   <td> <p> Área frontal de la imagen sobre un rectángulo relleno de negro sólido </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norm  </span> </p> </td> 
   <td> <p> Rectángulo de imagen opaco </p> </td> 
   <td> <p> Área frontal de la imagen </p> </td> 
   <td> <p> Área frontal de la imagen o capa </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invertir  </span> </p> </td> 
   <td> <p> Capa oculta </p> </td> 
   <td> <p> Área de fondo de la imagen </p> </td> 
   <td> <p> Área de fondo de la imagen o capa rellenada con negro sólido </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f36ad1af348e45aeb3eb336544df30b0}

Imagen o atributo de capa. Se aplica a la capa 0 si `layer=comp`. Si se especifica en una capa de efecto, el comando modifica la máscara heredada de la capa principal.

El comportamiento de `maskUse=` no está definido ni es compatible cuando se especifica con capas de texto o de color sólido cuando no se aplica ninguna máscara de imagen (especificada con `mask=` o `catalog::Mask`).

## Predeterminado {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Ejemplo {#section-daa371e9be5547368ff6772342acba0a}

Colorear el área de fondo de una imagen; el primer plano de la imagen se define con una imagen de máscara independiente. Esto se consigue colocando el fondo de la imagen coloreada en la parte superior si la imagen no ha sido modificada:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Véase también {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [máscara=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
