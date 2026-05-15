---
title: Barra de control
description: La barra de control es el área rectangular que contiene y se encuentra detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa y los controles de volumen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 685fad5a-a75a-4c0c-9038-de99d814f4be
TQID: 'https://experienceleague.adobe.com/1tSWpSM3wPGihSid3WocaUo8HD6BP4arexuws5XRTPA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 0%

---

# Barra de control{#control-bar}

La barra de control es el área rectangular que contiene y se encuentra detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa y los controles de volumen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barra de control siempre tiene la anchura total del visor disponible. CSS permite cambiar el color, la altura y la posición vertical en relación con el contenedor del visor de vídeo.

El siguiente selector de clase CSS controla el aspecto de la barra de control:

```
.s7interactivevideoviewer .s7controlbar
```

## Propiedades CSS de la barra de control {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> principales </p> </td> 
   <td colname="col2"> <p>Posición desde el borde superior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior </span> </p> </td> 
   <td colname="col2"> <p> Posición desde el borde inferior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura de la barra de control. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo de la barra de control. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar un visor de vídeo con una barra de control gris de 30 píxeles de altura y situada en la parte superior del contenedor del visor de vídeo.

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
