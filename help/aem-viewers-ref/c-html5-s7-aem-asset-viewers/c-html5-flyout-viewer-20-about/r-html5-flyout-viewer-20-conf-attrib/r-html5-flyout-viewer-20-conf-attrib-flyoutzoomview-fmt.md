---
description: nulo
seo-description: nulo
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 1ed18115-9e29-434a-a48d-40bf6b48fe6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica el formato de imagen que utilizará el componente para cargar imágenes desde el servidor de imágenes. Si el formato especificado termina con <span class="codeph"> "-alpha"</span>, el componente procesa las imágenes como contenido transparente. Para todos los demás formatos de imagen, el componente trata las imágenes como opacas. Tenga en cuenta que el componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para que sea completamente transparente, establezca la propiedad CSS <span class="codeph"> background-color</span> en <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`jpeg`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`fmt=png-alpha`
