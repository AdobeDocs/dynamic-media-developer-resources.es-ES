---
description: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
uuid: 61e6372c-bab9-4aac-a8a1-dffecc2e4903
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---


# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Especifica el formato de imagen que utiliza el componente para cargar imágenes desde el servidor de imágenes. Si el formato especificado termina con <span class="codeph"> -alfa</span>, el componente procesa las imágenes como contenido transparente. Para el resto de formatos de imagen, el componente trata las imágenes como opacas. Tenga en cuenta que el componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para que el fondo sea transparente, establezca la propiedad <span class="codeph"> background-color</span> CSS en <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt-png-alpha`
