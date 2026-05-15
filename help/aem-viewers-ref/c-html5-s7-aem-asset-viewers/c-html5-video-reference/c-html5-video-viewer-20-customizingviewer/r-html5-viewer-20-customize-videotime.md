---
title: Tiempo del vídeo
description: El tiempo del vídeo es la visualización numérica que muestra el tiempo y la duración actuales del vídeo que se está reproduciendo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83491281-aff4-411a-a5a2-42e2454fd375
TQID: 'https://experienceleague.adobe.com/gQ1V9iJ25WFB8HM2KiklXC2xHWMBQyuBFtQBVjsj7sI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 199
ht-degree: 0%

---

# Tiempo del vídeo{#video-time}

El tiempo del vídeo es la visualización numérica que muestra el tiempo y la duración actuales del vídeo que se está reproduciendo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La familia de fuentes de hora del vídeo, el tamaño de fuente y el color de fuente están entre las propiedades que CSS puede controlar. También se puede colocar mediante CSS en relación con la barra de control que la contiene.

El aspecto del tiempo del vídeo se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7videotime
```

## Propiedades CSS del tiempo del vídeo {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> principales </p> </td> 
   <td colname="col2"> <p>Posición desde el borde superior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecho </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde derecho, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> Ancho del control de tiempo del vídeo. Esta propiedad es necesaria para que Internet Explorer 8 o posterior funcione correctamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>La familia de fuentes que se utilizará para el texto de visualización del tiempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>El tamaño de fuente que se utilizará para el texto de visualización de tiempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>El color de fuente que se utilizará para el texto de visualización del tiempo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Establezca el tiempo del vídeo en gris claro (hexadecimal `#BBBBBB`), con un tamaño de 12 píxeles, situado a 15 píxeles de la parte superior de la barra de control y a 80 píxeles de los bordes derechos de la barra de control.

```
.s7videoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
