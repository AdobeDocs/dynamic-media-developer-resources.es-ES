---
title: FlyoutZoomView.fmt
description: Especifica el formato de imagen que utiliza el componente para cargar imágenes del servidor de imágenes.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Especifica el formato de imagen que utiliza el componente para cargar imágenes del servidor de imágenes.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Si el formato especificado termina con <span class="codeph"> -alpha</span>, el componente procesa las imágenes como contenido transparente. Para el resto de los formatos de imagen, el componente trata las imágenes como opacas. </p> <p>El componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para hacerlo transparente, establezca la propiedad CSS <span class="codeph"> background-color</span> en <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
