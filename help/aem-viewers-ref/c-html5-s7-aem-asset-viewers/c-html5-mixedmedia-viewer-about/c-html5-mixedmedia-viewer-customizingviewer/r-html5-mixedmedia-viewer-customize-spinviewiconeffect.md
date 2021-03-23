---
description: El indicador de giro se superpone en el área de vista de giro. Se muestra cuando la imagen se encuentra en estado de restablecimiento y también depende del parámetro iconeffect.
seo-description: El indicador de giro se superpone en el área de vista de giro. Se muestra cuando la imagen se encuentra en estado de restablecimiento y también depende del parámetro iconeffect.
seo-title: Efecto Icono de vista de giro
solution: Experience Manager
title: Efecto Icono de vista de giro
uuid: 33445a3d-51dc-47a4-a8d1-87d25ea001e1
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# Efecto del icono de vista de giro{#spin-view-icon-effect}

El indicador de giro se superpone en el área de vista de giro. Se muestra cuando la imagen se encuentra en estado de restablecimiento y también depende del parámetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7spinview .s7iconeffect
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
   <td colname="col2"> <p> Ilustración del indicador de giro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del indicador de giro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del indicador de giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

El indicador de giro es compatible con el selector de atributos `state`, que se establece en `spin_1D` en el caso de conjuntos de giros unidimensionales y en `spin_2D` en el caso de conjuntos de giros multidimensionales.

Ejemplo: para configurar un indicador de zoom de 100 x 100 píxeles.

```
.s7mixedmediaviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```

