---
title: Reproductor de vídeo
description: El reproductor de vídeo de recorte inteligente es el área rectangular en la que se muestra el contenido de vídeo dentro del visor.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Reproductor de vídeo{#video-player}

El reproductor de vídeo de recorte inteligente es el área rectangular en la que se muestra el contenido de vídeo dentro del visor.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si las dimensiones del vídeo que se está reproduciendo no coinciden con las dimensiones del reproductor de vídeo de recorte inteligente, el contenido del vídeo se centra dentro del área de visualización rectangular del reproductor de vídeo de recorte inteligente.

El siguiente selector de clase CSS controla el aspecto del reproductor de vídeo de recorte inteligente:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**Propiedades CSS del reproductor de vídeo de recorte inteligente**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo de la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

El mensaje de error que se muestra si el sistema no es capaz de reproducir el vídeo se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: Para configurar un visor de recorte inteligente de vídeo con el tamaño del reproductor de recorte inteligente de vídeo establecido en 512 x 288 píxeles.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

Los subtítulos cerrados se colocan en un contenedor interno dentro del reproductor de vídeo de recorte inteligente. La posición de ese contenedor está controlada por los operadores de colocación WebVTT admitidos. El propio texto de rótulo está dentro de ese contenedor y su estilo se controla con el siguiente selector de clases CSS:

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**Propiedades CSS de subtítulos opcionales**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Fondo de texto de subtítulo cerrado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color del texto de los subtítulos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p> Grosor de fuente de subtítulos opcionales. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p> Tamaño de fuente de subtítulos opcionales. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Fuente de subtítulos opcionales. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para configurar el texto de subtítulos para que sea de 14 píxeles, gris claro, Arial®, en un fondo negro semitransparente:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

El aspecto de la animación almacenada en búfer se controla con el siguiente selector de clase CSS:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
```

**Propiedades CSS del icono de espera**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> Anchura del icono de animación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> Altura del icono de animación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen restante </span> </p> </td> 
   <td colname="col2"> <p> Margen izquierdo del icono de animación, normalmente menos la mitad del ancho del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen superior </span> </p> </td> 
   <td colname="col2"> <p> Margen superior del icono de animación, normalmente menos la mitad de la altura del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p> Pintura del pomo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una animación de almacenamiento en búfer para que tenga 101 píxeles de ancho y 29 píxeles de alto:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
