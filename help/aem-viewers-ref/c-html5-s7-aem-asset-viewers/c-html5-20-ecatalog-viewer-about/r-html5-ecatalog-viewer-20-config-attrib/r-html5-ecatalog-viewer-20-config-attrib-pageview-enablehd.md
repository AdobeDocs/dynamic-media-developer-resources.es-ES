---
description: nulo
seo-description: nulo
seo-title: PageView.enableHD
solution: Experience Manager
title: PageView.enableHD
topic: Dynamic media
uuid: dcfb202d-6ed8-4cb9-9254-b8dcfe99cd00
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# PageView.enableHD{#pageview-enablehd}

` [PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> siempre|nunca|límite</span> </p> </td> 
   <td colname="col2"> <p> Habilite, limite o deshabilite la optimización para dispositivos donde <span class="codeph"> devicePixelRatio</span> es bueno que <span class="codeph"> 1</span>, es decir, dispositivos con pantalla de alta densidad como iPhone4 y dispositivos similares. Si está activo, el componente limita el tamaño de la solicitud de imagen IS como si el dispositivo solo tuviera una proporción de píxeles de <span class="codeph"> 1</span> y de esa manera se reduce el ancho de banda. </p> <p>Vea el ejemplo siguiente </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Si se utiliza la configuración de límite, el componente solo habilita la densidad de píxeles altos hasta el límite especificado. </p> <p>Consulte el ejemplo siguiente. </p> </td> 
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
   <th colname="col1" class="entry"> <p>Si la variable set es igual a </p> </th> 
   <th colname="col2" class="entry"> <p>Resultado </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> siempre</span> </p> </td> 
   <td colname="col2"> <p>Siempre se tiene en cuenta la densidad de píxeles de la pantalla/dispositivo. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Si la densidad de píxeles de la pantalla = 1, la imagen solicitada es 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Si la densidad de píxeles de la pantalla es 1,5, la imagen solicitada es 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Si la densidad de píxeles de la pantalla = 2, la imagen solicitada es 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> nunca</span> </p> </td> 
   <td colname="col2"> <p>Siempre utiliza una densidad de píxeles de 1 e ignora la capacidad HD del dispositivo. Por lo tanto, la imagen solicitada siempre es 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> límite&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>Se solicita una densidad de píxeles del dispositivo y se proporciona únicamente si la imagen resultante está por debajo del límite especificado. </p> <p>El número límite se aplica a la dimensión de anchura o altura. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Si el número límite es 1600 y la densidad de píxeles es 1,5, se muestra la imagen de 1500 x 1500. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Si el número límite es 1600 y la densidad de píxeles es 2, se mostrará la imagen de 1000 x 1000 porque la imagen de 2000 x 2000 supera el límite. </p> </li> 
     </ul> </p> <p><b>Práctica</b> recomendada: El número límite debe funcionar junto con la configuración de compañía para la imagen de tamaño máximo. Por lo tanto, establezca el número límite para que sea igual al tamaño máximo de imagen de la compañía. </p> </td> 
  </tr> 
 </tbody> 
</table>

