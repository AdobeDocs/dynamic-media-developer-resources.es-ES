---
title: recurso compartido twitter
description: La herramienta compartir de twitter consiste en un botón agregado al panel Compartir en redes sociales. Cuando se selecciona el botón, se redirige al usuario a un cuadro de diálogo para compartir proporcionado por un servicio social. La posición del botón se administra completamente mediante la herramienta Compartir en redes sociales.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5bcf6868-7ebb-43ec-971d-2be9e53650bb
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# recurso compartido twitter{#twitter-share}

La herramienta compartir de twitter consiste en un botón agregado al panel Compartir en redes sociales. Cuando se selecciona el botón, se redirige al usuario a un cuadro de diálogo para compartir proporcionado por un servicio social. La posición del botón se administra completamente mediante la herramienta Compartir en redes sociales.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

El aspecto del botón Compartir de Twitter se controla con el siguiente selector de clase CSS:

```
.s7smartcropvideoviewer .s7twittershare
```

**Propiedades CSS de la herramienta Twitter Share**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el `state` selector de atributos, que se puede utilizar para aplicar distintos aspectos a distintos estados de botón.

Es posible quitar el botón del panel Compartir en redes sociales mediante la configuración `display:none` Propiedad CSS en su clase CSS.

La información del objeto del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar un botón de uso compartido de Twitter de 28 x 28 píxeles y mostrar una imagen diferente para cada uno de los cuatro estados de botón diferentes:

```
.s7smartcropvideoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
