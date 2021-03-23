---
description: El visor muestra iconos de zonas interactivas en la vista principal en los lugares donde las zonas interactivas se crearon originalmente en Dynamic Media de AEM Assets, On Demand.
seo-description: El visor muestra iconos de zonas interactivas en la vista principal en los lugares donde las zonas interactivas se crearon originalmente en Dynamic Media de AEM Assets, On Demand.
seo-title: Puntos interactivos
solution: Experience Manager
title: Puntos interactivos
uuid: 79c4d128-e24a-43b0-8e18-13b588eb396e
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# Puntos interactivos{#hotspots}

El visor muestra iconos de zonas interactivas en la vista principal en los lugares donde las zonas interactivas se crearon originalmente en Dynamic Media de AEM Assets, On Demand.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del icono de zona interactiva se controla con el siguiente selector de clase CSS:

```
.s7interactiveimage .s7imagemapeffect .s7icon
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

