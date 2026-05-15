---
title: Botón Primera página
description: Al tocar o hacer clic en este botón, se lleva al usuario a la primera página del catálogo. Este botón aparece en la barra de control principal de los sistemas de escritorio y las tabletas; en los teléfonos móviles se añade a una barra de control secundaria. Puede cambiar el tamaño, la apariencia y la posición de este botón mediante CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: a84c8b20-93ea-4121-99b0-427e45ec0417
TQID: 'https://experienceleague.adobe.com/Bm8Nerva3tLsFiQ8o0ntopSnXB-gLGKnpg4zyeJcXkc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 0%

---

# Botón Primera página{#first-page-button}

Al pulsar o seleccionar este botón, el usuario accede a la primera página del catálogo. Este botón aparece en la barra de control principal de los sistemas de escritorio y las tabletas; en los teléfonos móviles se añade a una barra de control secundaria. Puede cambiar el tamaño, la apariencia y la posición de este botón mediante CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Propiedades CSS del área de visor principal**

El aspecto del botón se controla con el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton`

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
   <td colname="col2"> <p>Posición desde el borde superior de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecho </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde derecho de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dejó </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde izquierdo de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde inferior de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
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

Ejemplo: Para configurar un primer botón de página de 28 x 28 píxeles y colocado a 4 píxeles de la parte inferior y a 220 píxeles del borde izquierdo de la barra de control principal. Y, finalmente, muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes.

```
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton { 
bottom:4px; 
left:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/FirstPageButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/FirstPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/FirstPageButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/FirstPageButton_dark_disabled.png); 
}
```
