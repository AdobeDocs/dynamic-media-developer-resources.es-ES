---
title: Uso compartido de facebook
description: La herramienta Compartir de facebook consiste en un botón añadido al panel Compartir en Social . Cuando se selecciona el botón, el usuario se redirige a un cuadro de diálogo de uso compartido proporcionado por un servicio social. La posición del botón la gestiona completamente la herramienta de uso compartido de Social.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 343cde8b-796a-420f-abb7-268b3791a684
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Uso compartido de facebook{#facebook-share}

La herramienta Compartir de facebook consiste en un botón añadido al panel Compartir en Social . Cuando se selecciona el botón, el usuario se redirige a un cuadro de diálogo de uso compartido proporcionado por un servicio social. La posición del botón la gestiona completamente la herramienta de uso compartido de Social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

El aspecto del botón Compartir de Facebook se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7facebookshare
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
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

Es posible quitar el botón del panel Compartir en Social estableciendo la propiedad `display:none` CSS en su clase CSS.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Ejemplo** : para configurar un botón de uso compartido de Facebook de 28 x 28 píxeles, muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes:

```
.s7video360viewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7video360viewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7video360viewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7video360viewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
