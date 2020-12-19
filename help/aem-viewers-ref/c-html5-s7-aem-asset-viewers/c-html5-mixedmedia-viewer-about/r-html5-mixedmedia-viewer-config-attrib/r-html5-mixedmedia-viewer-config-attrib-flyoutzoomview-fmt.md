---
description: Especifica el formato de imagen que utiliza el componente para cargar imágenes desde el servidor de imágenes.
seo-description: Especifica el formato de imagen que utiliza el componente para cargar imágenes desde el servidor de imágenes.
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 6f6a69b4-d581-44ff-b089-ce9d0d0170bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Especifica el formato de imagen que utiliza el componente para cargar imágenes desde el servidor de imágenes.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Si el formato especificado termina con <span class="codeph"> -alpha</span>, el componente procesa las imágenes como contenido transparente. Para todos los demás formatos de imagen, el componente trata las imágenes como opacas. </p> <p>Tenga en cuenta que el componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para hacerlo completamente transparente, establezca la propiedad <span class="codeph"> color de fondo</span> CSS en <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
