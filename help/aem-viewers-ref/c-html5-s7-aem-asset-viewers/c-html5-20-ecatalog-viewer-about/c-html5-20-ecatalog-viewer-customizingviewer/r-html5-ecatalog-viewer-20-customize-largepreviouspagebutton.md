---
description: Al pulsar o hacer clic en este botón, el usuario llega a la página anterior del catálogo. Este botón aparece en la barra de control principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.
seo-description: Al pulsar o hacer clic en este botón, el usuario llega a la página anterior del catálogo. Este botón aparece en la barra de control principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.
seo-title: Botón Grande de la página anterior
solution: Experience Manager
title: Botón Grande de la página anterior
uuid: 12e12b82-88f2-4fbf-bbbb-dea027eb6775
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 2%

---


# Botón de página anterior grande{#large-previous-page-button}

Al pulsar o hacer clic en este botón, el usuario llega a la página anterior del catálogo. Este botón aparece en la barra de control principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del botón se controla con el siguiente selector de clase CSS:

`.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton`

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
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: para configurar un botón de página anterior grande de 56 x 56 píxeles, centrado verticalmente y anclado al borde izquierdo del visor, muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes.

```
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton { 
bottom:50%; 
margin-bottom:-28px; 
left:0px; 
width:56px; 
height:56px; 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/LeftButton_dark_up.png); 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/LeftButton_dark_over.png); 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/LeftButton_dark_down.png); 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/LeftButton_dark_disabled.png); 
}
```

