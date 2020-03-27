---
description: nulo
seo-description: nulo
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 570a9cca-17fa-44d5-b3bb-66ec19453cbc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica el formato de imagen que utilizará el componente para cargar imágenes desde el servidor de imágenes. Si el formato especificado termina con <span class="codeph"> -alpha</span>, el componente procesa las imágenes como contenido transparente. Para todos los demás formatos de imagen, el componente trata las imágenes como opacas. </p> <p>Tenga en cuenta que el componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para que sea completamente transparente, establezca la propiedad CSS <span class="codeph"> background-color</span> en <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
