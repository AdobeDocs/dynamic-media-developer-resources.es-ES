---
description: La herramienta Compartir Twitter consiste en un botón agregado al panel Compartir en redes sociales. Cuando se hace clic en el botón, se redirige al usuario a un cuadro de diálogo de uso compartido proporcionado por un servicio social. La posición del botón la gestiona completamente la herramienta Compartir en Social.
seo-description: La herramienta Compartir Twitter consiste en un botón agregado al panel Compartir en redes sociales. Cuando se hace clic en el botón, se redirige al usuario a un cuadro de diálogo de uso compartido proporcionado por un servicio social. La posición del botón la gestiona completamente la herramienta Compartir en Social.
seo-title: Compartir en Twitter
solution: Experience Manager
title: Compartir en Twitter
topic: Dynamic media
uuid: 75b8eab1-74fd-4c18-8556-c3cb17011cde
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Compartir en Twitter{#twitter-share}

La herramienta Compartir Twitter consiste en un botón agregado al panel Compartir en redes sociales. Cuando se hace clic en el botón, se redirige al usuario a un cuadro de diálogo de uso compartido proporcionado por un servicio social. La posición del botón la gestiona completamente la herramienta Compartir en Social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

El aspecto del botón Compartir de Twitter se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7twittershare
```

**Propiedades CSS de la herramienta para compartir Twitter**

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
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de `state` atributos, que se puede utilizar para aplicar diferentes apariencias a diferentes estados de botón.

Es posible quitar el botón del panel Compartir en Social estableciendo la propiedad CSS en su clase CSS `display:none` .

La información de objeto del botón se puede localizar. Consulte [Localización de los elementos](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de la interfaz de usuario para obtener más información.

Ejemplo: para configurar un botón Compartir en Twitter de 28 x 28 píxeles y mostrar una imagen diferente para cada uno de los cuatro estados de botón diferentes:

```
.s7ecatalogviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7ecatalogviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7ecatalogviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7ecatalogviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```

