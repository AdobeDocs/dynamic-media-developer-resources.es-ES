---
description: Especifica el formato de imagen que utiliza el componente para cargar imágenes desde el servidor de imágenes.
solution: Experience Manager
title: ZoomView.fmt
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---


# ZoomView.fmt{#zoomview-fmt}

Especifica el formato de imagen que utiliza el componente para cargar imágenes desde el servidor de imágenes.

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Si el formato especificado termina con <span class="codeph"> -alfa</span>, el componente procesa las imágenes como contenido transparente. Para el resto de formatos de imagen, el componente trata las imágenes como opacas. El componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para que sea transparente, establezca la propiedad <span class="codeph"> background-color</span> CSS en <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
