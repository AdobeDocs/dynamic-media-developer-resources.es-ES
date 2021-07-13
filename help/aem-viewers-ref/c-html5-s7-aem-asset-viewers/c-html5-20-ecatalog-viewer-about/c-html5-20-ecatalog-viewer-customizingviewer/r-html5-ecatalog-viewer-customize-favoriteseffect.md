---
description: El visor muestra los iconos de Favoritos sobre la vista principal en los lugares donde el usuario lo agregó originalmente.
solution: Experience Manager
title: Favoritos, efecto
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Developer,User
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# Favoritos, efecto{#favorites-effect}

El visor muestra los iconos de Favoritos sobre la vista principal en los lugares donde el usuario lo agregó originalmente.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del icono Favorito se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**Propiedades CSS del icono Favorito**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p> La imagen que se muestra para el icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del icono. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configuración de un icono Favoritos de 36 x 36 píxeles.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

En los sistemas de escritorio, el componente admite el selector de atributos `cursortype` que puede aplicar a la clase `.s7favoriteseffect` y controla el tipo del cursor en función de la acción seleccionada por el usuario. Se admiten los siguientes `cursortype` valores:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add  </span> </p> </td> 
   <td colname="col2"> <p>El usuario mostrado está agregando un nuevo icono Favorito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove  </span> </p> </td> 
   <td colname="col2"> <p>El usuario mostrado está eliminando un icono de Favorito existente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view  </span> </p> </td> 
   <td colname="col2"> <p>Se muestra en el modo de operación normal cuando la edición de Favoritos no está activa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: tener diferentes cursores del ratón para cada tipo de estado del componente.

```
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```
