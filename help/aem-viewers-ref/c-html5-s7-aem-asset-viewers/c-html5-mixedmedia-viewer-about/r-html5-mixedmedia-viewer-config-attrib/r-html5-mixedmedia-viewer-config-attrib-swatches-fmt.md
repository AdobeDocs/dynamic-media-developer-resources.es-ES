---
description: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
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

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt-png-alpha`
