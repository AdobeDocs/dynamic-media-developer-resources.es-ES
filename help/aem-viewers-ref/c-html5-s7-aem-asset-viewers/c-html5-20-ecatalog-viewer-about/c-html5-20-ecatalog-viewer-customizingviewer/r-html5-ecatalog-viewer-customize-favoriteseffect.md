---
description: El visor muestra los iconos de Favoritos sobre la vista principal en los lugares donde el usuario lo agregó originalmente.
seo-description: El visor muestra los iconos de Favoritos sobre la vista principal en los lugares donde el usuario lo agregó originalmente.
seo-title: Favoritos, efecto
solution: Experience Manager
title: Favoritos, efecto
topic: Dynamic media
uuid: b660b9fd-592b-4072-83c9-f70330ee19ab
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para el icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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

Ejemplo: configure un icono Favoritos de 36 x 36 píxeles.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

En sistemas de escritorio, el componente admite el selector de `cursortype` atributos que puede aplicar a la `.s7favoriteseffect` clase y controla el tipo del cursor en función de la acción del usuario seleccionado. The following `cursortype` values are supported:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>El usuario mostrado está agregando un nuevo icono Favorito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>El usuario mostrado está eliminando un icono de Favorito existente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_vista </span> </p> </td> 
   <td colname="col2"> <p>Se muestra en el modo de operación normal cuando la edición de Favoritos no está activa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: tiene diferentes cursores de ratón para cada tipo de estado del componente.

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

