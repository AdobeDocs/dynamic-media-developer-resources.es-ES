---
title: FlyoutZoomView.imagereload
description: Configura cómo el componente recupera nuevas imágenes para las vistas principal y flotante durante el cambio de tamaño.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configura cómo el componente recupera nuevas imágenes para las vistas principal y flotante durante el cambio de tamaño.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>Cuando se configura como <span class="codeph"> 0 </span>, el componente no carga imágenes nuevas durante el cambio de tamaño y la resolución de la imagen en la vista flotante no cambia. </p> <p>Cuando se configura como <span class="codeph"> 1 </span> permite especificar uno o más puntos de interrupción de anchura para la imagen cargada en la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> punto de interrupción, <span class="varname"> width </span>[; <span class="varname"> width </span>] </span> </p> </td> 
   <td colname="col2"> <p>Puntos de interrupción de ancho para la imagen cargada en la vista principal. El componente siempre utiliza el mejor tamaño para la carga inicial. Después de cambiar el tamaño, se asegura de que la imagen en la vista principal siempre se descargue con la anchura igual al punto de interrupción más grande más cercano y se reduzca la escala en el cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
