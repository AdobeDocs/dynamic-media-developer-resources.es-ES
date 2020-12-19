---
description: Ajuste el brillo. Reduce o aumenta el brillo de la imagen.
seo-description: Ajuste el brillo. Reduce o aumenta el brillo de la imagen.
seo-title: op_bright
solution: Experience Manager
title: op_bright
topic: Scene7 Image Serving - Image Rendering API
uuid: 751ec9e5-4a70-438d-950c-deff4db034b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---


# op_bright{#op-brightness}

Ajuste el brillo. Reduce o aumenta el brillo de la imagen.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de brillo (-100...+100 int). </p></td> 
 </tr> 
</table>

## Propiedades {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Omitido por capas de efectos. Las imágenes o capas CMYK se convierten a RGB antes de que se aplique la operación.

## Predeterminado {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, para no cambiar el brillo.

## Ejemplo {#section-c25f952f1b77409abb9ccf885862d75c}

Oscurecer ligeramente el fondo de una imagen para resaltar el contenido en primer plano:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
