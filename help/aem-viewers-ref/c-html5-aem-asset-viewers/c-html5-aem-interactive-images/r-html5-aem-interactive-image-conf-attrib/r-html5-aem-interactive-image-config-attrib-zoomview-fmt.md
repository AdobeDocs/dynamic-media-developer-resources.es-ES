---
title: ZoomView.fmt
description: Especifica el formato de imagen que utiliza el componente para cargar imágenes del servidor de imágenes.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 6a023abb-71c7-4db5-8d05-bf0a4b1fc3a0
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# ZoomView.fmt{#zoomview-fmt}

Especifica el formato de imagen que utiliza el componente para cargar imágenes del servidor de imágenes.

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Si el formato especificado termina con <span class="codeph"> -alpha</span>, el componente procesa las imágenes como contenido transparente. Para el resto de los formatos de imagen, el componente trata las imágenes como opacas. El componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para que sea transparente, configure el <span class="codeph"> background-color</span> Propiedad CSS a <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
