---
title: Puntos interactivos y mapas de imagen
description: El visor muestra los iconos de puntos interactivos en la vista principal en lugares donde los puntos interactivos se crearon originalmente en Dynamic Media of AEM Assets (bajo demanda).
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# Puntos interactivos y mapas de imagen{#hotspots-and-image-maps}

El visor muestra los iconos de puntos interactivos en la vista principal en lugares donde los puntos interactivos se crearon originalmente en Dynamic Media of AEM Assets (bajo demanda).

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área de visor principal**

El aspecto del icono del punto interactivo se controla con el siguiente selector de clase CSS:

```
.s7carouselviewer .s7imagemapeffect .s7icon
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Icono de punto interactivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p>Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Anchura del icono del punto interactivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del icono de punto interactivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configure un icono de punto interactivo de 56 x 56 píxeles que muestre una imagen diferente para cada uno de los dos estados de icono diferentes:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**Propiedades CSS de la región del mapa de imagen**

El aspecto del área del mapa de imagen se controla con el siguiente selector de clase CSS:

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de relleno de región de mapa de imagen. </p> <p>Especifique este color en <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> o <span class="codeph"> formatos RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de relleno de región de mapa de imagen. </p> <p>Especifique este color en <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> o <span class="codeph"> formatos RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p> Estilo de borde de región de mapa de imagen. Debe especificarse como " <span class="codeph"> anchura </span> <span class="codeph"> color sólido </span>", donde <span class="codeph"> anchura </span> se expresa en píxeles, y <span class="codeph"> color </span> se establece como <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> o <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configuración de una región de mapa de imagen transparente con un borde negro de un píxel:

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
