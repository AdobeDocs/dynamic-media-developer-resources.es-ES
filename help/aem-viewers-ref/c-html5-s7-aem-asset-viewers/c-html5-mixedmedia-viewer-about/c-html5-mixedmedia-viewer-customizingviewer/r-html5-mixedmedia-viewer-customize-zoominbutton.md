---
description: Al pulsar o hacer clic en este botón, se amplía la imagen de la vista principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.
solution: Experience Manager
title: Botón Ampliar
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de medios mixtos
role: Developer,Business Practitioner
exl-id: 663f9bb5-c432-4b34-ac76-a62826994a81
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 2%

---

# Botón Ampliar{#zoom-in-button}

Al pulsar o hacer clic en este botón, se amplía la imagen de la vista principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del botón se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7zoominbutton
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
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde superior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde derecho, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> izquierda </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde izquierdo, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde inferior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) para obtener más información.

Ejemplo: para configurar un botón de zoom de 32 x 32 píxeles, situado a seis píxeles del borde superior y derecho del visor, muestra una imagen diferente para cada uno de los cuatro estados de botón.

```
.s7mixedmediaviewer .s7zoominbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7zoominbutton [state='up'] { 
background-image:url(images/v2/ZoomInButton_dark_up.png); 
} 
.s7mixedmediaviewer .s7zoominbutton [state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png); 
} 
.s7mixedmediaviewer .s7zoominbutton [state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png); 
} 
.s7mixedmediaviewer .s7zoominbutton [state='disabled'] { 
background-image:url(images/v2/ZoomInButton_dark_disabled.png); 
}
```
