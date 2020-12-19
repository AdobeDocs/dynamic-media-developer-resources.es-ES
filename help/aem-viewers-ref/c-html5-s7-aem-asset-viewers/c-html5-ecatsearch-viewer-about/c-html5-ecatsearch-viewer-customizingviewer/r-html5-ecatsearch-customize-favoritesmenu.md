---
description: La lista desplegable del menú Favoritos aparece en la barra de control. Consta de un botón y un panel que se expande cuando un usuario hace clic o toca un botón. El panel contiene herramientas de Favoritos individuales.
seo-description: La lista desplegable del menú Favoritos aparece en la barra de control. Consta de un botón y un panel que se expande cuando un usuario hace clic o toca un botón. El panel contiene herramientas de Favoritos individuales.
seo-title: Menú Favoritos
solution: Experience Manager
title: Menú Favoritos
topic: Dynamic media
uuid: 46de2a74-690e-4010-8a71-54206dd02fd0
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Menú Favoritos{#favorites-menu}

La lista desplegable del menú Favoritos aparece en la barra de control. Consta de un botón y un panel que se expande cuando un usuario hace clic o toca un botón. El panel contiene herramientas de Favoritos individuales.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La posición y el tamaño del menú Favoritos de la interfaz de usuario del visor se controlan con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7favoritesmenu
```

**Propiedades CSS del botón de menú Favoritos**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento desde la parte superior de la barra de control. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Distancia al botón siguiente de la izquierda o del lado izquierdo de la barra de control si éste es el primer botón de una fila. </p> </td> 
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

Ejemplo: configure un menú Favoritos que se posicione cuatro píxeles desde la parte superior de la barra de control y diez píxeles desde el botón más cercano a la izquierda y tenga un tamaño de 28 x 28 píxeles.

```
.s7ecatalogsearchviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

El aspecto del botón de menú Favoritos se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton
```

**Propiedades CSS del botón Favoritos**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes apariencias a distintos estados de botones.

La información de objeto del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: configure un botón de menú Favoritos que muestre una imagen diferente para cada uno de los cuatro estados de botón diferentes.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

El aspecto del panel que contiene los iconos de Favoritos individuales se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel
```

**Propiedades CSS del panel de menús Favoritos**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configure un panel para que tenga un color transparente.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

