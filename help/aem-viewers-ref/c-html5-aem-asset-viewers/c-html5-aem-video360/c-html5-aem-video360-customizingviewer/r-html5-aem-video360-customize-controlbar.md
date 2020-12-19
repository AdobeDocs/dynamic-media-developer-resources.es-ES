---
description: La barra de control es el área rectangular que contiene y se sitúa detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa, los controles de volumen, etc.
seo-description: La barra de control es el área rectangular que contiene y se sitúa detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa, los controles de volumen, etc.
seo-title: Barra de control
solution: Experience Manager
title: Barra de control
topic: Dynamic media
uuid: 328e34f1-9e60-4056-9a8a-e9292fb65605
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# Barra de control{#control-bar}

La barra de control es el área rectangular que contiene y se sitúa detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa, los controles de volumen, etc.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barra de control siempre toma toda la anchura del visor disponible. Es posible cambiar el color, la altura y la posición vertical mediante CSS en relación con el contenedor del visor de vídeo.

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

**Ejemplo** : Para configurar un visor de vídeo con una barra de control gris de 30 píxeles de alto y situada en la parte superior del contenedor del visor de vídeo.

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

