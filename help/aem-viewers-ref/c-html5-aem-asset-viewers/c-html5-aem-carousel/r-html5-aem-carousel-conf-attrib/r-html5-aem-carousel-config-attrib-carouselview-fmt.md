---
title: CarouselView.fmt
description: CarouselView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: a43ca095-2a59-4a0c-a460-f465cbd4ed5f
TQID: 'https://experienceleague.adobe.com/99Ro91SwAOW1pEl1NIsq5pyCiEfNPGFueyX6oDpouuU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 4%

---

# CarouselView.fmt{#carouselview-fmt}

`[CarouselView.|<containerId>_carouselView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica el formato de imagen que utiliza el componente para cargar imágenes del servidor de imágenes. </p> <p>Si el formato especificado termina con <span class="codeph"> -alpha</span>, el componente procesa las imágenes como contenido transparente. </p> <p>Para el resto de los formatos de imagen, el componente trata las imágenes como opacas. El componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para hacerlo transparente, establezca la propiedad CSS <span class="codeph"> background-color</span> en <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
