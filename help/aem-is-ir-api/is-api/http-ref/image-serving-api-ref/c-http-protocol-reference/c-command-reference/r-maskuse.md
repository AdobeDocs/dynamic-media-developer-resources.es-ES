---
title: maskUse
description: Uso de máscara de imagen. Especifica cómo se utiliza la máscara o el canal alfa de la imagen para las operaciones en la imagen (por ejemplo, colorear=). Cuando se especifica en una capa de efecto, permite aplicar el efecto al área de fondo de la capa principal o a todo el rectángulo de la capa principal.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# maskUse{#maskuse}

Uso de máscara de imagen. Especifica cómo se utiliza la máscara o el canal alfa de la imagen para las operaciones en la imagen (por ejemplo, colorear=). Cuando se especifica en una capa de efecto, permite aplicar el efecto al área de fondo de la capa principal o a todo el rectángulo de la capa principal.

`maskUse=norm|invert|off`

La siguiente tabla ilustra el efecto de `maskUse=` según la disponibilidad y el tipo de la máscara (canal alfa) asociada a la imagen de capa.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> valor</b> </th> 
   <th class="entry"> <b> Sin máscara</b> </th> 
   <th class="entry"> <b> alfa no asociado (o imagen de máscara independiente)</b> </th> 
   <th class="entry"> <b> alfa asociado (premultiplicado) </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> de </span> </p> </td> 
   <td> <p> Rectángulo de imagen opaco </p> </td> 
   <td> <p> Rectángulo de imagen opaco </p> </td> 
   <td> <p> Área frontal de la imagen sobre rectángulo rellena de negro sólido </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norma </span> </p> </td> 
   <td> <p> Rectángulo de imagen opaco </p> </td> 
   <td> <p> Área frontal de la imagen </p> </td> 
   <td> <p> Área frontal de la imagen o capa </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invertir </span> </p> </td> 
   <td> <p> Capa oculta </p> </td> 
   <td> <p> Área de fondo de la imagen </p> </td> 
   <td> <p> Área de fondo de la imagen o capa rellena con negro sólido </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f36ad1af348e45aeb3eb336544df30b0}

Atributo de imagen o capa. Se aplica a la capa 0 si `layer=comp`. Si se especifica en una capa de efecto, el comando modifica la máscara heredada de la capa principal.

El comportamiento de `maskUse=` no está definido y no se admite cuando se especifica con capas de color sólido o de texto cuando no se aplica ninguna máscara de imagen (especificada con `mask=` o `catalog::Mask`).

## Predeterminado {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Ejemplo {#section-daa371e9be5547368ff6772342acba0a}

Colorear el área de fondo de una imagen; el primer plano de la imagen se define mediante una imagen de máscara independiente. Esto se logra superponiendo el fondo de imagen coloreado en la parte superior si la imagen no modificada:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Véase también {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [máscara=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
