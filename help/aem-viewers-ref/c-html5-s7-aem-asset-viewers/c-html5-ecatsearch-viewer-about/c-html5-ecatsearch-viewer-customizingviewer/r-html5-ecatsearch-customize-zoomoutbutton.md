---
title: Botón de alejar
description: Al seleccionar este botón, se amplía una imagen de la vista principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, la apariencia y la posición de este botón mediante CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: a4c2eb32-819c-45a1-ac03-44e78ebd042b
TQID: 'https://experienceleague.adobe.com/F8Rr-y24ZZAFFFUmGYpFxtthxur0Tuf3VrxPyUFlqB4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# Botón de alejar{#zoom-out-button}

Al seleccionar este botón, se amplía una imagen de la vista principal. Este botón no se muestra en los teléfonos móviles para ahorrar espacio en la pantalla. Puede cambiar el tamaño, la apariencia y la posición de este botón mediante CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área de visor principal**

El aspecto del botón se controla con el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7zoomoutbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> principales </p> </td> 
   <td colname="col2"> <p>Posición desde el borde superior de la barra de control principal, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecho </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde derecho de la barra de control principal, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dejó </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde izquierdo de la barra de control principal, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde inferior de la barra de control principal, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

La información del objeto del botón se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: Para configurar un botón de alejamiento de 28 x 28 píxeles, y colocado a 4 píxeles de la parte inferior y a 75 píxeles del borde derecho de la barra de control principal. Y, finalmente, muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes.

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
