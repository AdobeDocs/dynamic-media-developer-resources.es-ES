---
description: PageView.enableHD
solution: Experience Manager
title: PageView.enableHD
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Developer,User
exl-id: f03762f2-87db-4284-ba59-9ece8caa0d09
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 3%

---

# PageView.enableHD{#pageview-enablehd}

` [PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Habilite, limite o deshabilite la optimización para dispositivos en los que <span class="codeph"> devicePixelRatio</span> sea bueno que <span class="codeph"> 1</span>, es decir, dispositivos con una pantalla de alta densidad como iPhone4 y dispositivos similares. Si está activo, el componente limita el tamaño de la solicitud de imagen IS como si el dispositivo solo tuviera una relación de píxeles de <span class="codeph"> 1</span> y de esa manera se reduzca el ancho de banda. </p> <p>Consulte el ejemplo siguiente </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Si se utiliza la configuración de límite, el componente permite una alta densidad de píxeles sólo hasta el límite especificado. </p> <p>Consulte el ejemplo siguiente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-38b878e38caa439bb462d4fa637afdaa}

Opcional.

## Predeterminado {#section-50b22de303c1432094530e6583132c02}

`limit,1500`

## Ejemplo {#section-09433488774245d985acef6c0341ece0}

Los siguientes son los resultados esperados al utilizar este atributo de configuración con el visor y el tamaño del visor es de 1000 x 1000:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Si la variable configurada es igual a </p> </th> 
   <th colname="col2" class="entry"> <p>Resultado </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> siempre</span> </p> </td> 
   <td colname="col2"> <p>Siempre se tiene en cuenta la densidad de píxeles de la pantalla/dispositivo. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Si la densidad de píxeles de la pantalla = 1, la imagen solicitada es 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Si la densidad de píxeles de la pantalla = 1,5, la imagen solicitada es 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Si la densidad de píxeles de la pantalla = 2, la imagen solicitada es 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> nunca</span> </p> </td> 
   <td colname="col2"> <p>Siempre utiliza una densidad de píxeles de 1 e ignora la capacidad HD del dispositivo. Por lo tanto, la imagen solicitada es siempre 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> límite&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>La densidad de píxeles del dispositivo se solicita y se sirve solo si la imagen resultante está por debajo del límite especificado. </p> <p>El número límite se aplica a la dimensión de anchura o altura. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Si el número límite es 1600 y la densidad de píxeles es 1,5, se sirve la imagen de 1500 x 1500. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Si el número límite es 1600 y la densidad de píxeles es 2, se sirve la imagen de 1000 x 1000 porque la imagen de 2000 x 2000 supera el límite. </p> </li> 
     </ul> </p> <p><b>Práctica recomendada</b>: El número límite debe funcionar junto con la configuración de la empresa para la imagen de tamaño máximo. Por lo tanto, establezca el número límite para que sea igual al tamaño máximo de imagen de la empresa. </p> </td> 
  </tr> 
 </tbody> 
</table>
