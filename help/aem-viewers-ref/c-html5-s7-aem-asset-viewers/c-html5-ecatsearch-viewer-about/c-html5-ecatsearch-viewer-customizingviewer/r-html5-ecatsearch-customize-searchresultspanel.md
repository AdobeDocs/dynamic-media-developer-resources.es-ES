---
description: El panel de resultados de búsqueda consta del cuadro de entrada de búsqueda en la parte superior y del área principal donde se muestran los mensajes informativos o los resultados de búsqueda.
seo-description: El panel de resultados de búsqueda consta del cuadro de entrada de búsqueda en la parte superior y del área principal donde se muestran los mensajes informativos o los resultados de búsqueda.
seo-title: Panel de resultados de búsqueda
solution: Experience Manager
title: Panel de resultados de búsqueda
topic: Dynamic media
uuid: 43d8e003-79f7-4e41-98d7-b362ab7180ea
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Panel de resultados de búsqueda{#search-results-panel}

El panel de resultados de búsqueda consta del cuadro de entrada de búsqueda en la parte superior y del área principal donde se muestran los mensajes informativos o los resultados de búsqueda.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

Cuando el panel está activo, la interfaz de usuario del visor está cubierta por un relleno semitransparente. El color y la opacidad de este relleno se controlan con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de la superposición. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidad  </span> </p> </td> 
   <td colname="col2"> <p>Opacidad del color. </p> </td> 
  </tr> 
 </tbody> 
</table>

El panel de resultados de búsqueda siempre ocupa toda la altura del visor disponible. Sin embargo, puede configurar la anchura. Puede establecer la anchura en un valor de píxel absoluto, que es una configuración predeterminada para los puntos de interrupción de tamaño medio y grande. O bien, puede establecer la anchura en 100 % para que el panel de resultados de búsqueda ocupe toda el área del visor. El ancho del panel se controla mediante el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**Propiedad CSS del espacio de resultados de búsqueda**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho del espacio de resultados de búsqueda. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un panel de resultados de búsqueda de 250 píxeles de ancho en puntos de interrupción grandes y medianos y utilizar un panel de tamaño completo en un punto de interrupción de tamaño pequeño:

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

La parte superior del panel de resultados de búsqueda está dedicada al cuadro de entrada de búsqueda. El relleno en los lados del cuadro de entrada está controlado por el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**Propiedades CSS del contenedor de entrada de búsqueda**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Relleno alrededor del cuadro de entrada. </p> </td> 
  </tr> 
 </tbody> 
</table>

El campo de entrada de búsqueda está controlado por el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**Propiedades CSS del campo de entrada de búsqueda**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del campo de entrada de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno-izquierda  </span> </p> </td> 
   <td colname="col2"> <p> El margen interior entre los límites del campo de entrada y el texto de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde del campo de entrada de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Margen del campo de entrada de búsqueda </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de la fuente de texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un campo de entrada de búsqueda con una altura de 0 píxeles y una fuente de texto de 14 píxeles:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

El botón de búsqueda a la izquierda del campo de entrada de búsqueda en forma de &quot;cristal de aspecto&quot; de forma predeterminada está controlado por el siguiente selector de clase CSS:

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**Propiedades CSS del botón de entrada de búsqueda**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón de entrada de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón de entrada de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>La dirección URL de la imagen del icono de "luce vidrio". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-size  </span> </p> </td> 
   <td colname="col2"> <p>El tamaño del icono "de cristal". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde del botón de entrada de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>Margen del botón de entrada de búsqueda. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un botón de búsqueda con el icono de &quot;cristal&quot; de 26 x 26 píxeles; 30 píxeles de tamaño con un borde de 1 píxel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

El panel de resultados de búsqueda puede mostrar un mensaje de texto cuando se llama por primera vez a la función. También muestra un mensaje al usuario cuando su búsqueda no arrojó ningún resultado. En todos los casos, el texto aparece en la parte principal del panel de resultados de búsqueda y está controlado por el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**Propiedades CSS de la información de búsqueda**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Color del texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nombre de la fuente de texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>Alineación de texto horizontal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño del texto de fuente. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este panel de texto admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes estilos a distintos mensajes de texto. En particular, `state='prompt'` corresponde al mensaje de texto que se muestra cuando se llama al panel por primera vez; `state='results'` corresponde al texto con información sobre las visitas de búsqueda; y `state='no_results'` corresponde al texto mostrado cuando la consulta de búsqueda no arrojó ningún resultado.

El texto del mensaje se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: para configurar un panel de texto que utilice una fuente gris de 18 píxeles:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

Los resultados de la búsqueda se representan como una sola columna o fila de miniaturas para las páginas con visitas de búsqueda. El espaciado entre las miniaturas de los resultados de búsqueda se controla con el siguiente selector de clase CSS:

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**Propiedades CSS de las celdas de miniaturas**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p> Tamaño del margen vertical alrededor de cada miniatura. El espaciado de miniaturas real es igual a la suma de los márgenes superior e inferior definidos para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar el espaciado de 10 píxeles:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

El aspecto de las miniaturas individuales se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**Propiedades CSS de la miniatura**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Anchura de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde de la miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar miniaturas de 215 x 129 píxeles, tenga un borde predeterminado de color gris claro y un borde seleccionado de color gris oscuro:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

El aspecto de la etiqueta de miniatura se controla con el siguiente selector de clase CSS:

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**Propiedades CSS de la etiqueta**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Color de texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nombre de la fuente de texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de la fuente de texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar etiquetas que utilicen fuentes Helvetica de 12 píxeles, gris:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

En los sistemas que utilizan la entrada del ratón, aparecen dos botones de desplazamiento en la parte inferior del panel de resultados de búsqueda para que el usuario se desplace por los resultados de la búsqueda. El aspecto de los botones de desplazamiento hacia arriba y hacia abajo se controla con los siguientes selectores de clase CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

No es posible colocar botones de desplazamiento con las propiedades CSS top, left, bottom y right. En su lugar, la lógica del visor las coloca automáticamente.

**Propiedades CSS de los botones de desplazamiento hacia arriba y hacia abajo**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón de desplazamiento. </p> </td> 
  </tr> 
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
>Este botón admite el selector de atributos `state`, que se puede utilizar para aplicar diferentes apariencias a los estados de los botones `"up"`, `"down"`, `"over"` y `"disabled"`.

La información del objeto de botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: para configurar un botón de desplazamiento hacia arriba de 125 x 35 píxeles y con una ilustración diferente para cada estado:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```

