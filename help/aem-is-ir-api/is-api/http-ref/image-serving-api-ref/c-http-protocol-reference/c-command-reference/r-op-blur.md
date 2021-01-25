---
description: Desenfocar imagen. Aplica un filtro de desenfoque a los datos de la imagen.
seo-description: Desenfocar imagen. Aplica un filtro de desenfoque a los datos de la imagen.
seo-title: op_blur
solution: Experience Manager
title: op_blur
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---


# op_blur{#op-blur}

Desenfocar imagen. Aplica un filtro de desenfoque a los datos de la imagen.

`op_blur= *`radio`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radio</span> </p> </td> 
  <td class="stentry"> <p>Radio del filtro de desenfoque en píxeles (0,100 real). </p></td> 
 </tr> 
</table>

*`radius`* está en píxeles en relación con la imagen compuesta. También se utiliza para calar efectos de capa.

## Propiedades {#section-92573fe2c07746a7bab93a81fc3d208d}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`.

## Predeterminado {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, sin efecto de desenfoque.

## Ejemplo {#section-1ebacde68388492eb108ae0fcd7424db}

Desenfocar el fondo de una imagen. `catalog::MaskPath` hace referencia a una imagen de máscara independiente. Tenga en cuenta que `layer=0`debe especificarse explícitamente; de lo contrario, `op_blur` se aplicaría a toda la imagen compuesta.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
