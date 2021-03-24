---
description: Ajuste el brillo. Reduce o aumenta el brillo de la imagen.
solution: Experience Manager
title: op_bright
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
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

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por capas de efecto. Las imágenes o capas CMYK se convierten a RGB antes de aplicar la operación.

## Predeterminado {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, para no cambiar el brillo.

## Ejemplo {#section-c25f952f1b77409abb9ccf885862d75c}

Oscurecer ligeramente el fondo de una imagen para resaltar el contenido en primer plano:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
