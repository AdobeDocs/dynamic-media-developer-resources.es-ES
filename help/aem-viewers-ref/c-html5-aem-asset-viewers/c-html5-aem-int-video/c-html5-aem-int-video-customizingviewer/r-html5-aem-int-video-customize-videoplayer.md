---
description: El reproductor de vídeo es el área rectangular en la que se muestra el contenido del vídeo en el visor.
seo-description: El reproductor de vídeo es el área rectangular en la que se muestra el contenido del vídeo en el visor.
seo-title: Reproductor de vídeo
solution: Experience Manager
title: Reproductor de vídeo
topic: Dynamic media
uuid: ff0f78b1-ff88-47b8-a118-4e0b3e75f341
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Reproductor de vídeo{#video-player}

El reproductor de vídeo es el área rectangular en la que se muestra el contenido del vídeo en el visor.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si las dimensiones del vídeo que se está reproduciendo no coinciden con las del reproductor de vídeo, el contenido del vídeo se centra en el área de visualización rectangular del reproductor de vídeo.

El siguiente selector de clase CSS controla el aspecto del reproductor de vídeo:

```
.s7interactivevideoviewer .s7videoplayer
```

**Propiedades CSS del reproductor de vídeo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo de la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puede localizar el mensaje de error que se muestra en los casos en los que el sistema no puede reproducir el vídeo.

Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Ejemplo: Para configurar un visor de vídeo con el tamaño del reproductor de vídeo definido en 512 x 288 píxeles.

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

Los subtítulos cerrados se colocan en un contenedor interno dentro del reproductor de vídeo. La posición de ese contenedor está controlada por los operadores de posicionamiento WebVTT admitidos. El texto del rótulo está dentro de ese contenedor y su estilo se controla con el siguiente selector de clase CSS:

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**Propiedades CSS de los subtítulos opcionales**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Fondo de texto de subtítulos opcionales. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Cierre el color del texto del rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p> Peso de fuente de subtítulos opcionales. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> Tamaño de fuente de subtítulos opcionales. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Fuente de subtítulos opcionales. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-5b82913ff3c44b7b8187969cb15e9560}

Para configurar el texto de los subtítulos opcionales en 14 píxeles, gris claro, Arial, sobre un fondo negro semitransparente:

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

El aspecto de la animación de almacenamiento en búfer se controla con el siguiente selector de clase CSS:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
```

**Propiedades CSS del icono de espera**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Anchura del icono de animación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altura del icono de animación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Icono de animación margen izquierdo, normalmente menos la mitad de la anchura del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Margen superior del icono de animación, normalmente menos la mitad de la altura del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Ilustración del botón. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una animación de almacenamiento en búfer para que tenga 101 píxeles de ancho y 29 píxeles de alto:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

