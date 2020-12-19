---
description: La hora del vídeo es la visualización numérica que muestra la hora y la duración actuales del vídeo que se está reproduciendo.
seo-description: La hora del vídeo es la visualización numérica que muestra la hora y la duración actuales del vídeo que se está reproduciendo.
seo-title: Tiempo de vídeo
solution: Experience Manager
title: Tiempo de vídeo
topic: Dynamic media
uuid: f8ba615f-661a-4750-bdf7-559650d464af
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Tiempo de vídeo{#video-time}

La hora del vídeo es la visualización numérica que muestra la hora y la duración actuales del vídeo que se está reproduciendo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Entre las propiedades que puede controlar CSS se encuentran la familia de fuentes de vídeo, el tamaño de fuente y el color de fuente. También puede colocarse, en relación con la barra de control que la contiene, mediante CSS.

El aspecto del tiempo de vídeo se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7videotime
```

## Propiedades CSS del tiempo de vídeo {#css-properties-of-video-time}

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
   <td colname="col2"> <p> Ancho del control de tiempo del vídeo. Esta propiedad es necesaria para que Internet Explorer 8 o bueno funcionen correctamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes que se va a utilizar para mostrar el texto durante el tiempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>El tamaño de fuente que se va a utilizar para mostrar el texto durante el tiempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>El color de fuente que se usará para mostrar el texto durante el tiempo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** : defina el tiempo del vídeo en gris claro (hexadecimal  `#BBBBBB`), con un tamaño de 12 píxeles, situado 15 píxeles desde la parte superior de la barra de control y 80 píxeles desde los bordes superior y derecho de la barra de control.

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

