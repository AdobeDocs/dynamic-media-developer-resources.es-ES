---
description: El reproductor de vídeo es el área rectangular en la que se muestra el contenido de vídeo dentro del visor.
seo-description: El reproductor de vídeo es el área rectangular en la que se muestra el contenido de vídeo dentro del visor.
seo-title: Reproductor de vídeo
solution: Experience Manager
title: Reproductor de vídeo
uuid: 2748c3d3-b974-4e54-8218-a2ec9e31a668
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 1%

---


# Reproductor de vídeo{#video-player}

El reproductor de vídeo es el área rectangular en la que se muestra el contenido de vídeo dentro del visor.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si las dimensiones del vídeo que se está reproduciendo no coinciden con las dimensiones del reproductor, el contenido del vídeo se centra dentro del área de visualización rectangular del reproductor de vídeo.

El siguiente selector de clase CSS controla el aspecto del reproductor de vídeo:

```
.s7videoviewer .s7videoplayer
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

Se puede localizar el mensaje de error que se muestra si el sistema no es capaz de reproducir el vídeo. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar un visor de vídeo con el tamaño del reproductor de vídeo establecido en 512 x 288 píxeles.

```
.s7videoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

Los subtítulos se colocan en un contenedor interno dentro del reproductor de vídeo. La posición de ese contenedor está controlada por los operadores de posición WebVTT admitidos. El texto del rótulo en sí está dentro de ese contenedor y su estilo se controla con el siguiente selector de clase CSS:

`. s7videoviewer .s7 videoplayer .s7caption`

**Propiedades CSS de subtítulos**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Fondo de texto de subtítulos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Cierre el color del texto del rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p> Grosor de fuente de subtítulos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> Tamaño de fuente de subtítulos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Fuente de subtítulos. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar el texto de los subtítulos cerrados en 14 píxeles, gris claro, Arial, sobre un fondo negro semitransparente:

```
.s7videoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

El aspecto de la animación de almacenamiento en búfer se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Ilustración del botón. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una animación de almacenamiento en búfer para que tenga 101 píxeles de ancho y 29 píxeles de alto:

```
.s7videoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

