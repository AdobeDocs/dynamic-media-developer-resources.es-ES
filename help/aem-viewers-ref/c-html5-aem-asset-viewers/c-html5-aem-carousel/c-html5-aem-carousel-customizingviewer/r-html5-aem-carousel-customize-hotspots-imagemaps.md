---
description: El visor muestra iconos de zonas interactivas en la vista principal en los lugares donde las zonas interactivas se crearon originalmente en Dynamic Media de AEM Assets, On Demand.
seo-description: El visor muestra iconos de zonas interactivas en la vista principal en los lugares donde las zonas interactivas se crearon originalmente en Dynamic Media de AEM Assets, On Demand.
seo-title: Puntos interactivos y mapas de imágenes
solution: Experience Manager
title: Puntos interactivos y mapas de imágenes
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 1%

---


# Puntos interactivos y mapas de imágenes{#hotspots-and-image-maps}

El visor muestra iconos de zonas interactivas en la vista principal en los lugares donde las zonas interactivas se crearon originalmente en Dynamic Media de AEM Assets, On Demand.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del icono de zona interactiva se controla con el siguiente selector de clase CSS:

```
.s7carouselviewer .s7imagemapeffect .s7icon
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
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p>Icono de zona interactiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p>Sitúe el elemento en el sprite de ilustración si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del icono de zona interactiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del icono de zona interactiva. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configure un icono de zona interactiva de 56 x 56 píxeles que muestre una imagen diferente para cada uno de los dos estados de icono diferentes:

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

El aspecto de la región del mapa de imagen se controla con el siguiente selector de clase CSS:

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fondo  </span> </p> </td> 
   <td colname="col2"> <p>Color de relleno de la región del mapa de imagen. </p> <p>Especifique este color en los formatos <span class="codeph"> #RGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> o <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de relleno de la región del mapa de imagen. </p> <p>Especifique este color en los formatos <span class="codeph"> #RGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> o <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p> Estilo del borde de la región del mapa de imágenes. Debe especificarse como " <span class="codeph"> anchura </span> <span class="codeph"> color sólido </span>", donde <span class="codeph"> anchura </span> se expresa en píxeles, y <span class="codeph"> color </span> se establece como <span class="codeph"> #RGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> 1/&gt; o <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
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

