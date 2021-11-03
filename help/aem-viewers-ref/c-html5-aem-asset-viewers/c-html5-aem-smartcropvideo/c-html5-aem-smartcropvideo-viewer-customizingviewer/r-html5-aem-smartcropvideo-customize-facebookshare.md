---
description: La herramienta Compartir de facebook consiste en un botón añadido al panel Compartir en Social . Cuando se hace clic en el botón, el usuario se redirige a un cuadro de diálogo de uso compartido proporcionado por un servicio social. La posición del botón la gestiona completamente la herramienta de uso compartido de Social.
solution: Experience Manager
title: Uso compartido de facebook
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 6b7e043f-6a9f-48ba-b811-3c94fe5c32f1
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Uso compartido de facebook{#facebook-share}

La herramienta Compartir de facebook consiste en un botón añadido al panel Compartir en Social . Cuando se hace clic en el botón, el usuario se redirige a un cuadro de diálogo de uso compartido proporcionado por un servicio social. La posición del botón la gestiona completamente la herramienta de uso compartido de Social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

El aspecto del botón Compartir de Facebook se controla con el siguiente selector de clase CSS:

```
.s7smartcropvideoviewer .s7facebookshare
```

**Propiedades CSS de la herramienta de uso compartido de Facebook**

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
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite la variable `state` selector de atributos, que se puede utilizar para aplicar diferentes aspectos a distintos estados de botones.

Es posible quitar el botón del panel Compartir en Social configurando `display:none` Propiedad CSS en su clase CSS.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar un botón de uso compartido de Facebook de 28 x 28 píxeles y muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes:

```
.s7smartcropvideoviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
