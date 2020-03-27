---
description: La herramienta Compartir Facebook consiste en un botón agregado al panel Compartir en redes sociales. Cuando se hace clic en el botón, se redirige al usuario a un cuadro de diálogo de uso compartido proporcionado por un servicio social. La posición del botón la gestiona completamente la herramienta Compartir en Social.
seo-description: La herramienta Compartir Facebook consiste en un botón agregado al panel Compartir en redes sociales. Cuando se hace clic en el botón, se redirige al usuario a un cuadro de diálogo de uso compartido proporcionado por un servicio social. La posición del botón la gestiona completamente la herramienta Compartir en Social.
seo-title: Uso compartido de Facebook
solution: Experience Manager
title: Uso compartido de Facebook
topic: Dynamic media
uuid: 8575fde4-4d03-4b87-a628-ff06ff8c91c9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Uso compartido de Facebook{#facebook-share}

La herramienta Compartir Facebook consiste en un botón agregado al panel Compartir en redes sociales. Cuando se hace clic en el botón, se redirige al usuario a un cuadro de diálogo de uso compartido proporcionado por un servicio social. La posición del botón la gestiona completamente la herramienta Compartir en Social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

El aspecto del botón Compartir de Facebook se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7facebookshare
```

**Propiedades CSS de la herramienta para compartir Facebook**

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
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de `state` atributos, que se puede utilizar para aplicar diferentes apariencias a diferentes estados de botón.

Es posible quitar el botón del panel Compartir en Social estableciendo la propiedad CSS en su clase CSS `display:none` .

La información de objeto del botón se puede localizar. Consulte [Localización de los elementos](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)de la interfaz de usuario.

**Ejemplo** : para configurar un botón Compartir de Facebook de 28 x 28 píxeles y mostrar una imagen diferente para cada uno de los cuatro estados de botón diferentes:

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

