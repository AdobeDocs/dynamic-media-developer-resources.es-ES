---
description: Según el valor del parámetro mode, el visor muestra los iconos de mapa de imagen sobre la vista principal en lugares donde los mapas se crearon originalmente en Scene7 Publishing System o representa las regiones exactas que coinciden con la forma de los mapas de imagen originales.
seo-description: Según el valor del parámetro mode, el visor muestra los iconos de mapa de imagen sobre la vista principal en lugares donde los mapas se crearon originalmente en Scene7 Publishing System o representa las regiones exactas que coinciden con la forma de los mapas de imagen originales.
seo-title: Efecto de mapa de imagen
solution: Experience Manager
title: Efecto de mapa de imagen
topic: Dynamic media
uuid: 8bafaec3-500c-4a1f-b511-bff125daab7f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 1%

---


# Efecto de mapa de imagen{#image-map-effect}

Según el valor del parámetro mode, el visor muestra los iconos de mapa de imagen sobre la vista principal en lugares donde los mapas se crearon originalmente en Scene7 Publishing System o representa las regiones exactas que coinciden con la forma de los mapas de imagen originales.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del icono de mapa de imagen se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>La clase CSS `s7mapoverlay` utilizada para aplicar estilo a los iconos de mapas de imagen en el pasado ya no se utiliza; utilice `s7icon` en su lugar.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Icono de mapa de imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del icono del mapa de imagen en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del icono del mapa de imagen en píxeles. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El icono de mapa de imagen admite el selector de atributos `state`, que puede utilizar para aplicar diferentes apariencias a los estados de icono de `default` y `active`.

Ejemplo: configure un icono de mapa de imagen de 28 x 28 píxeles que muestre una imagen diferente para cada uno de los dos estados de icono diferentes.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Consulte también [Compatibilidad con mapas de imagen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

El aspecto de la región del mapa de imagen se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fondo  </span> </p> </td> 
   <td colname="col2"> <p> Color de relleno de la región del mapa de imagen. </p> <p>Especificado en formato #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de relleno de la región del mapa de imagen. </p> <p>Especificado en formato #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p> Estilo del borde de la región del mapa de imagen. </p> <p>Se especifica como <span class="codeph"> <span class="varname"> ancho </span> sólido <span class="varname"> color </span> </span>, donde <span class="codeph"> <span class="varname"> ancho </span> </span> se expresa en píxeles y <span class="codeph"> <span class="varname"> color </span> </span> se establece como #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configure una región de mapa de imagen transparente con un borde negro de `1` píxeles:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

