---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: fd81cd48-9990-4659-a52c-7abdbc95a0e3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 1%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> siempre|nunca|límite</span> </p> </td> 
   <td colname="col2"> <p> Activar, limitar o desactivar la optimización para dispositivos donde <span class="codeph"> devicePixelRatio</span> es mayor que <span class="codeph"> 1</span>, es decir, dispositivos con visualización de alta densidad como iPhone4 y similares. Si está activo, el componente limita el tamaño de la solicitud de imagen del servicio de imágenes como si el dispositivo solo tuviera una proporción de píxeles de <span class="codeph"> 1</span> y, de esa manera, se reduce el ancho de banda. </p> <p>Consulte el ejemplo siguiente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Si se utiliza el ajuste de límite, el componente solo permite una alta densidad de píxeles hasta el límite especificado. </p> <p>Consulte el ejemplo siguiente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`limit,1500`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

Los siguientes son los resultados esperados cuando se utiliza este atributo de configuración con el visor y el tamaño del visor es de 1000 x 1000:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Si la variable establecida es igual a </p> </th> 
   <th colname="col2" class="entry"> <p>Resultado </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> siempre</span> </p> </td> 
   <td colname="col2"> <p>La densidad de píxeles de la pantalla o del dispositivo siempre se tiene en cuenta. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Si la densidad de píxeles de la pantalla = 1, la imagen solicitada es 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Si la densidad de píxeles de la pantalla = 1,5, la imagen solicitada es de 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Si la densidad de píxeles de la pantalla = 2, la imagen solicitada es de 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> nunca</span> </p> </td> 
   <td colname="col2"> <p>Siempre utiliza una densidad de píxeles de 1 e ignora la capacidad HD del dispositivo. Por lo tanto, la imagen solicitada siempre es 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> límite&lt;número&gt;</span> </p> </td> 
   <td colname="col2"> <p>Se solicita una densidad de píxeles de dispositivo y se sirve solo si la imagen resultante está por debajo del límite especificado. </p> <p>El número límite se aplica tanto a la dimensión de anchura como a la de altura. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Si el número límite es 1600 y la densidad de píxeles es 1,5, se proporciona la imagen de 1500 x 1500. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Si el número límite es 1600 y la densidad de píxeles es 2, la imagen de 1000 x 1000 se proporciona porque la imagen de 2000 x 2000 supera el límite. </p> </li> 
     </ul> </p> <p><b>Práctica recomendada</b>: El número límite debe funcionar con la configuración de la empresa para la imagen de tamaño máximo. Por lo tanto, establezca el número límite para que sea igual a la configuración del tamaño máximo de imagen de la empresa. </p> </td> 
  </tr> 
 </tbody> 
</table>
