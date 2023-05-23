---
title: Botón Página anterior
description: Al tocar o hacer clic en este botón, se lleva al usuario a la página anterior del catálogo. Este botón aparece en la barra de control principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, la apariencia y la posición de este botón mediante CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: cc0e8c18-f9c1-4451-9fbe-3b082f78a7ec
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 2%

---

# Botón Página anterior{#previous-page-button}

Al pulsar o seleccionar este botón, se lleva al usuario a la página anterior del catálogo. Este botón aparece en la barra de control principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, la apariencia y la posición de este botón mediante CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del botón se controla con el siguiente selector de clase CSS:

`.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
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
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el `state` selector de atributos, que se puede utilizar para aplicar distintos aspectos a distintos estados de botón.

La información del objeto del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: Para configurar un botón de página anterior de 28 x 28 píxeles y situado a 4 píxeles de la parte inferior y a 250 píxeles del borde derecho de la barra de control principal. Y, finalmente, muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes.

```
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton { 
bottom:4px; 
left:250px; 
width:32px; 
height:32px; 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/ToolBarLeftButton_dark_up.png); 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/ToolBarLeftButton_dark_over.png); 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/ToolBarLeftButton_dark_down.png); 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/ToolBarLeftButton_dark_disabled.png); 
}
```
