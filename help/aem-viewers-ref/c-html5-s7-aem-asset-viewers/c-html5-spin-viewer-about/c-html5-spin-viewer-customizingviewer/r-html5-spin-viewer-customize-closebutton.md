---
title: Botón Cerrar
description: Al pulsar o hacer clic en este botón, se cierra la página web contenedora. Este botón solo aparece si el parámetro close button está establecido en 1. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e2f8e45a-5b24-45fa-a009-fc3221a65c15
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 3%

---

# Botón Cerrar{#close-button}

Al seleccionar este botón, se cierra la página web contenedora. Este botón solo aparece si el parámetro close button está establecido en 1. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del botón se controla con el siguiente selector de clase CSS:

```
.s7spinviewer .s7closebutton
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
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p>Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite la variable `state` selector de atributos, que se puede utilizar para aplicar diferentes aspectos a distintos estados de botones.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98) para obtener más información.

Ejemplo: para configurar un botón Cerrar de 32 x 32 píxeles y colocar seis píxeles desde el borde superior y derecho del visor. Finalmente, muestra una imagen diferente para cada uno de los cuatro estados de botones diferentes.

```
.s7spinviewer .s7closebutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7spinviewer .s7closebutton [state='up'] { 
background-image:url(images/v2/CloseButton_dark_up.png); 
} 
.s7spinviewer .s7closebutton [state='over'] {  
background-image:url(images/v2/CloseButton_dark_over.png); 
} 
.s7spinviewer .s7closebutton [state='down'] {  
background-image:url(images/v2/CloseButton_dark_down.png); 
} 
.s7spinviewer .s7closebutton [state='disabled'] { 
background-image:url(images/v2/CloseButton_dark_disabled.png); 
}
```
