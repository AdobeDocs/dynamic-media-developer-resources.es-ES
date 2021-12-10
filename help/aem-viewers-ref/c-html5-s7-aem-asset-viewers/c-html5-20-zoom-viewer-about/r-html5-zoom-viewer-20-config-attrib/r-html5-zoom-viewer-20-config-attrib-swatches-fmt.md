---
title: Swatches.fmt
description: Swatches.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8b47839a-ef3b-45ae-8e8d-5c9391d71d44
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Especifica el formato de imagen que utiliza el componente para cargar imágenes desde el servidor de imágenes. Si el formato especificado termina con <span class="codeph"> -alfa</span>, el componente procesa las imágenes como contenido transparente. Para el resto de formatos de imagen, el componente trata las imágenes como opacas. El componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para que el fondo sea transparente, defina la variable <span class="codeph"> background-color</span> Propiedad CSS a <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt-png-alpha`
