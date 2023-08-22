---
title: op_blur
description: Desenfocar imagen. Aplica un filtro de desenfoque a los datos de imagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# op_blur{#op-blur}

Desenfocar imagen. Aplica un filtro de desenfoque a los datos de imagen.

`op_blur= *`radio`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radio</span> </p> </td> 
  <td class="stentry"> <p>Radio de filtro de desenfoque en píxeles (real 0..100). </p></td> 
 </tr> 
</table>

*`radius`* está en píxeles con relación a la imagen compuesta. También se utiliza para desvanecer efectos de capa.

## Propiedades {#section-92573fe2c07746a7bab93a81fc3d208d}

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`.

## Predeterminado {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, sin efecto de desenfoque.

## Ejemplo {#section-1ebacde68388492eb108ae0fcd7424db}

Desenfocar el fondo de una imagen. Se hace referencia a una imagen de máscara independiente mediante `catalog::MaskPath`. Tenga en cuenta que `layer=0`debe especificarse explícitamente; en caso contrario `op_blur` se aplicaría a toda la imagen compuesta.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
