---
description: La hora del vídeo es la visualización numérica que muestra la hora y la duración actuales del vídeo que se está reproduciendo.
solution: Experience Manager
title: Tiempo de vídeo
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de medios mixtos
role: Developer,Business Practitioner
exl-id: 5efae314-5f37-4afc-9b9e-3108a8529e50
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---

# Tiempo de vídeo{#video-time}

La hora del vídeo es la visualización numérica que muestra la hora y la duración actuales del vídeo que se está reproduciendo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La familia de fuentes de tiempo de vídeo, el tamaño de fuente y el color de fuente están entre las propiedades que puede controlar CSS. También se puede posicionar, en relación con la barra de control que la contiene, mediante CSS.

El aspecto del tiempo de vídeo se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7videotime
```

## Propiedades CSS de la hora del vídeo {#css-properties-of-video-time}

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
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>La familia de fuentes que se usará para el texto de visualización de la hora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>El tamaño de fuente que se utilizará para el texto de visualización de la hora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color de fuente que se usará para el texto de visualización de la hora. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Establezca el tiempo de vídeo en gris claro (hexadecimal `#BBBBBB`), con un tamaño de 12 píxeles, posicione 15 píxeles desde la parte superior de la barra de control y 80 píxeles desde los bordes derechos de la barra de control.

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
