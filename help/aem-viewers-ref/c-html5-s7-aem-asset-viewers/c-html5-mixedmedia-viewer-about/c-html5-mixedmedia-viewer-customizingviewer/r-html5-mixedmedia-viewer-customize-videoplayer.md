---
title: Reproductor de vídeo
description: El reproductor de vídeo es el área rectangular en la que se muestra el contenido de vídeo dentro del visor.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2f92d76e-3104-4ad8-9426-662275492251
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---

# Reproductor de vídeo{#video-player}

El reproductor de vídeo es el área rectangular en la que se muestra el contenido de vídeo dentro del visor.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si las dimensiones del vídeo que se reproduce no coinciden con las del reproductor de vídeo, el contenido del vídeo se centra dentro del área de visualización rectangular del reproductor de vídeo.

El siguiente selector de clase CSS controla el aspecto del reproductor de vídeo:

```
.s7mixedmediaviewer .s7videoplayer
```

**Propiedades CSS del reproductor de vídeo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo del reproductor de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El mensaje de error que se muestra si el sistema no puede reproducir el vídeo se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) para obtener más información.

Ejemplo: Para hacer transparente el reproductor de vídeo:

```
.s7mixedmediaviewer .s7videoplayer { 
 background-color: transparent; 
}
```

Los subtítulos se colocan en un contenedor interno dentro del reproductor de vídeo. La posición de ese contenedor está controlada por los operadores de colocación WebVTT admitidos. El texto del pie de ilustración en sí está dentro de ese contenedor; su estilo se controla con el siguiente selector de clases CSS:

```
.s7mixedmediaviewer .s7videoplayer .s7caption
```

**Propiedades CSS de los subtítulos**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Fondo de texto de rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color del texto del rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para configurar el texto del pie de ilustración como Arial® gris claro de 14 píxeles en un fondo negro semitransparente:

```
.s7mixedmediaviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

El aspecto de la animación almacenada en búfer se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Anchura del icono de animación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altura del icono de animación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> Margen izquierdo del icono de animación, normalmente menos la mitad del ancho del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Margen superior del icono de animación, normalmente menos la mitad de la altura del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Pintura del pomo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para configurar una animación de almacenamiento en búfer para que tenga 101 píxeles de ancho y 29 píxeles de alto:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
