---
title: Tiempo del vídeo
description: El tiempo del vídeo es la visualización numérica que muestra el tiempo y la duración actuales del vídeo que se está reproduciendo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 78657fd2-e805-4047-be0a-592143025986
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---

# Tiempo del vídeo{#video-time}

El tiempo del vídeo es la visualización numérica que muestra el tiempo y la duración actuales del vídeo que se está reproduciendo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La familia de fuentes de hora del vídeo, el tamaño de fuente y el color de fuente están entre las propiedades que CSS puede controlar. También se puede colocar mediante CSS en relación con la barra de control que la contiene.

El aspecto del tiempo del vídeo se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7videotime
```

## Propiedades CSS del tiempo del vídeo {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde superior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde derecho, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho del control de tiempo del vídeo. Esta propiedad es necesaria para que Internet Explorer 8 o bueno funcione correctamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>La familia de fuentes que se utilizará para el texto de visualización del tiempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>El tamaño de fuente que se utilizará para el texto de visualización de tiempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>El color de fuente que se utilizará para el texto de visualización del tiempo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** - Establecer el tiempo de vídeo en gris claro (hexadecimal) `#BBBBBB`), con un tamaño de 12 píxeles, colocados a 15 píxeles de la parte superior de la barra de control y a 80 píxeles de los bordes superior y derecho de la barra de control.

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
