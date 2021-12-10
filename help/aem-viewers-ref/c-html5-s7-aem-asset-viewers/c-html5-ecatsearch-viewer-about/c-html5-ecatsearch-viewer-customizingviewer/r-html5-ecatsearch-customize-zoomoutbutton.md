---
title: Botón Reducir
description: Al seleccionar este botón, se reduce la imagen de la vista principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: a4c2eb32-819c-45a1-ac03-44e78ebd042b
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 2%

---

# Botón Reducir{#zoom-out-button}

Al seleccionar este botón, se reduce la imagen de la vista principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del botón se controla con el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7zoomoutbutton`

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
   <td colname="col2"> <p>Posición desde el borde superior de la barra de control principal, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde derecho de la barra de control principal, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> izquierda </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde izquierdo de la barra de control principal, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde inferior de la barra de control principal, incluido el relleno. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite la variable `state` selector de atributos, que se puede utilizar para aplicar diferentes aspectos a distintos estados de botones.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: Configurar un botón de alejamiento de 28 x 28 píxeles y colocarlo 4 píxeles desde la parte inferior y 75 píxeles desde el borde derecho de la barra de control principal. Finalmente, muestra una imagen diferente para cada uno de los cuatro estados de botones diferentes.

```
.s7ecatalogsearchviewer .s7zoomoutbutton { 
bottom:4px; 
right:75px; 
width:28px; 
height:28px; 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='up'] { 
background-image:url(images/v2/ZoomOutButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='over'] {  
background-image:url(images/v2/ZoomOutButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='down'] {  
background-image:url(images/v2/ZoomOutButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='disabled'] { 
background-image:url(images/v2/ZoomOutButton_dark_disabled.png); 
}
```
