---
description: Configura cómo el componente obtiene nuevas imágenes para la vista principal y flotante durante el cambio de tamaño.
seo-description: Configura cómo el componente obtiene nuevas imágenes para la vista principal y flotante durante el cambio de tamaño.
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic Media
uuid: 5cded4cb-7b02-47da-9e2d-b236548cc61d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configura cómo el componente obtiene nuevas imágenes para la vista principal y flotante durante el cambio de tamaño.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`anchura de anchura`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>Cuando se establece en <span class="codeph"> 0 </span>, el componente no carga imágenes nuevas durante el cambio de tamaño y la resolución de imágenes en la vista flotante no cambia. </p> <p>Cuando se establece en <span class="codeph"> 1 </span> permite especificar uno o más puntos de interrupción de anchura para la imagen cargada en la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> punto de interrupción,  <span class="varname"> ancho  </span>[;  <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p>Puntos de interrupción de ancho para la imagen cargada en la vista principal. El componente utilizará siempre el mejor tamaño para la carga inicial. Después de cambiar el tamaño, se asegurará de que la imagen de la vista principal siempre se descargue con el ancho igual al punto de interrupción más grande más cercano y se reduzca la escala en el cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
