---
description: Al pulsar o hacer clic en este botón, se devuelve al usuario a la diapositiva anterior del conjunto de carrusel. Este botón no se muestra en los dispositivos táctiles. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.
seo-description: Al pulsar o hacer clic en este botón, se devuelve al usuario a la diapositiva anterior del conjunto de carrusel. Este botón no se muestra en los dispositivos táctiles. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.
seo-title: diapositiva anterior
solution: Experience Manager
title: diapositiva anterior
uuid: 733fa270-ce95-4493-9d31-f7f638d8368d
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 2%

---


# diapositiva anterior{#previous-slide}

Al pulsar o hacer clic en este botón, se devuelve al usuario a la diapositiva anterior del conjunto de carrusel. Este botón no se muestra en los dispositivos táctiles. Puede cambiar el tamaño, el aspecto y la posición de este botón mediante CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del botón se controla con el siguiente selector de clase CSS:

`.s7carouselviewer .s7panleftbutton`

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
   <td colname="col2"> <p>Posición desde la parte superior del borde del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p>Posición a la derecha del borde del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> izquierda </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la izquierda del borde del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la parte inferior del borde del visor. </p> </td> 
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
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>Tipo de cursor. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md) para obtener más información.

Ejemplo: para configurar un botón de diapositiva anterior de 60 x 60 píxeles, situado a 10 píxeles del borde izquierdo del visor y centrado verticalmente, muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes.

```
.s7carouselviewer .s7panleftbutton { 
 bottom: 50%; 
 left: 10px; 
 background-size:60px; 
 cursor: pointer; 
 } 
.s7carouselviewer.s7mouseinput .s7panleftbutton { 
 width:60px; 
 height:60px; 
 margin-bottom: -20px; 
} 
.s7carouselviewer.s7mouseinput .s7panleftbutton[state]  { 
    background-image: url(../../viewers/s7viewers/html5/images/v2/CarouselDotsLeftButton_dark_sprite.png); 
} 
 
.s7carouselviewer.s7mouseinput .s7panleftbutton[state='up'] { background-position: -0px -60px;  } 
.s7carouselviewer.s7mouseinput .s7panleftbutton[state='over'] { background-position: -0px -0px; } 
.s7carouselviewer.s7mouseinput .s7panleftbutton[state='down'] { background-position: -0px -0px; } 
.s7carouselviewer.s7mouseinput .s7panleftbutton[state='disabled'] { background-position: -0px -60px; }
```

