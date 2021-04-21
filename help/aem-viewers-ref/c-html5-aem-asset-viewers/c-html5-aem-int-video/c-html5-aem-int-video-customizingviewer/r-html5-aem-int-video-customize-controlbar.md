---
description: La barra de control es el área rectangular que contiene y se encuentra detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa, los controles de volumen, etc.
solution: Experience Manager
title: Barra de control
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 685fad5a-a75a-4c0c-9038-de99d814f4be
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---

# Barra de control{#control-bar}

La barra de control es el área rectangular que contiene y se encuentra detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa, los controles de volumen, etc.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barra de control siempre toma toda la anchura del visor disponible. CSS puede cambiar su color, altura y posición vertical en relación con el contenedor del visor de vídeo.

El siguiente selector de clase CSS controla el aspecto de la barra de control:

```
.s7interactivevideoviewer .s7controlbar
```

## Propiedades CSS de la barra de control {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde superior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p> Posición desde el borde inferior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de la barra de control. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo de la barra de control. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar un visualizador de vídeo con una barra de control gris de 30 píxeles de altura y situada en la parte superior del contenedor del visualizador de vídeo.

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
