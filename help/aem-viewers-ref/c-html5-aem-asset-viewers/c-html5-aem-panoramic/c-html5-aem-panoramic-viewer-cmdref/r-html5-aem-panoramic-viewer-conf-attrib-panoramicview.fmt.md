---
title: PanoramicView.fmt
description: Especifica el formato de imagen que utiliza el componente para cargar imágenes del servidor de imágenes.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

Especifica el formato de imagen que utiliza el componente para cargar imágenes del servidor de imágenes. Si el formato especificado termina con &quot;-alpha&quot;, el componente procesa las imágenes como transparentes. Para el resto de los formatos de imagen, el componente trata las imágenes como opacas. Tenga en cuenta que el componente tiene un fondo transparente de forma predeterminada. Por lo tanto, para que sea opaco, establezca el `background-color` Propiedad CSS a `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> Especifica el formato de imagen que utilizará el componente para cargar imágenes del servidor de imágenes. Si el formato especificado termina con "-alpha", el componente procesa las imágenes como transparentes; para el resto de los formatos de imagen, el componente trata las imágenes como opacas. Tenga en cuenta que el componente tiene un fondo transparente de forma predeterminada, por lo que para que sea opaco, establezca la propiedad CSS background-color en el color deseado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
