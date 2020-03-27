---
description: La posición del botón se administra completamente mediante el menú Favoritos.
seo-description: La posición del botón se administra completamente mediante el menú Favoritos.
seo-title: Botón Vista de todos los favoritos
solution: Experience Manager
title: Botón Vista de todos los favoritos
topic: Dynamic media
uuid: f9fd2110-d225-4eba-8e21-acc9c0e1dfd4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Botón Vista de todos los favoritos{#view-all-favorites-button}

La posición del botón se administra completamente mediante el menú Favoritos.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del botón Vista de todos los favoritos se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7viewallfavoritebutton
```

**Propiedades CSS del botón Quitar favorito**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite los selectores de atributos `state` y `selected` atributos, que se pueden utilizar para aplicar diferentes apariencias a distintos estados de botón. En particular, `selected='true'` corresponde al estado en el que un usuario puede agregar un nuevo icono de favorito haciendo clic o tocando. `selected='false'` corresponde al modo de operación normal cuando un usuario puede aplicar zoom, desplazarse e intercambiar páginas.

La información de objeto del botón se puede localizar. Consulte [Localización de los elementos](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de la interfaz de usuario para obtener más información.

Ejemplo: para configurar un botón Vista Todos los favoritos de 28 x 28 píxeles y muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes cuando se selecciona o no se selecciona.

```
.s7ecatalogviewer .s7viewallfavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_up.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_down.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_disabled.png); 
}
```

