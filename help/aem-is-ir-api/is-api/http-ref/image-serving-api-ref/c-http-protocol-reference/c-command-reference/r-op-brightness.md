---
title: op_bright
description: Ajuste el brillo. Reduce o aumenta el brillo de la imagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# op_bright{#op-brightness}

Ajuste el brillo. Reduce o aumenta el brillo de la imagen.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste del brillo (-100...+100 int). </p></td> 
 </tr> 
</table>

## Propiedades {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por las capas de efecto. Las imágenes o capas CMYK se convierten en RGB antes de que se aplique la operación.

## Predeterminado {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, sin cambio de brillo.

## Ejemplo {#section-c25f952f1b77409abb9ccf885862d75c}

Oscurezca ligeramente el fondo de una imagen para resaltar el contenido en primer plano:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
