---
description: El indicador de zoom se superpone en el área de vista principal. Se muestra cuando la imagen está en estado de restablecimiento y también depende del parámetro iconeffect.
seo-description: El indicador de zoom se superpone en el área de vista principal. Se muestra cuando la imagen está en estado de restablecimiento y también depende del parámetro iconeffect.
seo-title: Icono, efecto
solution: Experience Manager
title: Icono, efecto
uuid: 9e8c0c6f-2c45-4acb-9acb-5b8494bfc69b
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# Icono, efecto{#icon-effect}

El indicador de zoom se superpone en el área de vista principal. Se muestra cuando la imagen está en estado de restablecimiento y también depende del parámetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7pageview .s7iconeffect
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Ilustración del indicador de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Zoom de la anchura del indicador en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del indicador de zoom en píxeles. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El efecto Icono es compatible con el selector de atributos `media-type`, que puede utilizar para aplicar distintos efectos de icono en distintos dispositivos. En concreto, `media-type='standard'` corresponde a sistemas de escritorio en los que se utiliza normalmente la entrada del ratón y `media-type='multitouch'` corresponde a dispositivos con entrada táctil.

Ejemplo: para configurar un indicador de zoom de 100 x 100 píxeles con diferentes características para sistemas de escritorio y dispositivos táctiles.

```
.s7ecatalogviewer .s7pageview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```

