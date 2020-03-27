---
description: La barra de control es el área rectangular que contiene y se sitúa detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa, los controles de volumen, etc.
seo-description: La barra de control es el área rectangular que contiene y se sitúa detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa, los controles de volumen, etc.
seo-title: Barra de control
solution: Experience Manager
title: Barra de control
topic: Dynamic media
uuid: 7b7dccb3-6c64-4342-aac7-82c769561902
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Barra de control{#control-bar}

La barra de control es el área rectangular que contiene y se sitúa detrás de todos los controles de interfaz de usuario disponibles para el visor de vídeo, como el botón de reproducción/pausa, los controles de volumen, etc.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barra de control siempre toma toda la anchura del visor disponible. Es posible cambiar el color, la altura y la posición vertical mediante CSS en relación con el contenedor del visor de vídeo.

El siguiente selector de clase CSS controla el aspecto de la barra de control:

```
.s7mixedmediaviewer .s7controlbar
```

## Propiedades CSS de la barra de control {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de la barra de control. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo de la barra de control. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar un visor de medios mixtos con una barra de control gris de 30 píxeles de alto.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

