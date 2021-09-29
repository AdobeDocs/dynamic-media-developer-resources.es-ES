---
title: Barra de control
description: La barra de control es el área rectangular que contiene y se encuentra detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa y los controles de volumen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# Barra de control{#control-bar}

La barra de control es el área rectangular que contiene y se encuentra detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa y los controles de volumen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barra de control siempre toma toda la anchura del visor disponible. CSS puede cambiar su color, altura y posición vertical en relación con el contenedor del visor de vídeo.

El siguiente selector de clase CSS controla el aspecto de la barra de control:

```
.s7video360viewer .s7controlbar
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

**Ejemplo** : para configurar un visualizador de vídeo con una barra de control gris de 30 píxeles de altura y situada en la parte superior del contenedor del visualizador de vídeo.

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
