---
title: Diapositiva anterior
description: Al tocar o hacer clic en este botón, se devuelve al usuario a la diapositiva anterior del conjunto de carrusel. Este botón no se muestra en dispositivos táctiles. Puede cambiar el tamaño, la apariencia y la posición de este botón mediante CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f780e62e-7238-4cc6-b382-3a21043e1079
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Diapositiva anterior{#previous-slide}

Al seleccionar este botón, el usuario vuelve a la diapositiva anterior del conjunto de carrusel. Este botón no se muestra en dispositivos táctiles. Puede cambiar el tamaño, la apariencia y la posición de este botón mediante CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Propiedades CSS del área de visor principal**

El aspecto del botón se controla con el siguiente selector de clase CSS:

`.s7carouselviewer .s7panleftbutton`

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
   <td colname="col2"> <p>Posición desde la parte superior del borde del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecho </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la derecha del borde del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dejó </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la izquierda del borde del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la parte inferior del borde del visor. </p> </td> 
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
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte también <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Tipo de cursor. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

La información del objeto del botón se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md) para obtener más información.

Por ejemplo, supongamos que desea configurar un botón de diapositiva anterior de 60 x 60 píxeles. Se debe colocar a diez píxeles del borde izquierdo del visor y centrarlo verticalmente. Y desea que muestre una imagen diferente para cada uno de los cuatro estados de botón diferentes.

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
