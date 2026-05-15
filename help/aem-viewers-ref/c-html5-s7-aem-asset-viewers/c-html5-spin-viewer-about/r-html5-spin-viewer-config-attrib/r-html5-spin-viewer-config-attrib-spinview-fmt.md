---
title: SpinView.fmt
description: SpinView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 3927d626-db16-4d30-80d3-5f63c3e9a110
TQID: 'https://experienceleague.adobe.com/W8G9RnHoOVzh6oADHULe91atj33j1SEZz-a-yqFQv-Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 4%

---

# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica el formato de imagen que utiliza el componente para cargar imágenes del servidor de imágenes. Si el formato especificado termina con <span class="codeph"> -alpha</span>, el componente procesa las imágenes como contenido transparente. Para el resto de los formatos de imagen, el componente trata las imágenes como opacas. El componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para hacerlo transparente, establezca la propiedad CSS <span class="codeph"> background-color</span> en <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`jpeg`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`fmt=png-alpha`
