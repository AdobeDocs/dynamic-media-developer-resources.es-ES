---
title: Efecto de mapa de imagen
description: Según el valor del parámetro mode, el visor muestra iconos de mapa de imagen sobre la vista principal en lugares donde los mapas se crearon originalmente en Dynamic Media Classic. O bien, procesa regiones exactas que coinciden con la forma de los mapas de imagen originales.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3816118f-4eb7-4436-9f54-155dde077734
source-git-commit: 6087b48b898e93e605c3873cbd5132b74d04225f
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---

# Efecto de mapa de imagen{#image-map-effect}

Según el valor del parámetro mode, el visor muestra iconos de mapa de imagen sobre la vista principal en lugares donde los mapas se crearon originalmente en Dynamic Media Classic. O bien, procesa regiones exactas que coinciden con la forma de los mapas de imagen originales.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del icono de mapa de imagen se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>El `s7mapoverlay` La clase CSS utilizada para aplicar estilo a los iconos de mapa de imagen en el pasado ya no se utiliza. Use `s7icon` en su lugar.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Icono de mapa de imagen ilustrado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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
>El icono de mapa de imagen admite `state` selector de atributos, que puede utilizar para aplicar diferentes aspectos a los estados de icono de `default` y `active`.

Ejemplo: configure un icono de mapa de imagen de 28 x 28 píxeles que muestre una imagen diferente para cada uno de los dos estados de icono diferentes.

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Consulte también [Compatibilidad con mapas de imagen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

El aspecto del área del mapa de imagen se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fondo </span> </p> </td> 
   <td colname="col2"> <p> Color de relleno de región de mapa de imagen. </p> <p>Especificado en formato #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Color de relleno de región de mapa de imagen. </p> <p>Especificado en formato #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p> Estilo de borde de región de mapa de imagen. </p> <p>Especificado como <span class="codeph"> <span class="varname"> anchura </span> sólido <span class="varname"> color </span> </span>, donde <span class="codeph"> <span class="varname"> anchura </span> </span> se expresa en píxeles y <span class="codeph"> <span class="varname"> color </span> </span> se define como #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configuración de una región de mapa de imagen transparente con `1` borde negro en píxeles :

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
