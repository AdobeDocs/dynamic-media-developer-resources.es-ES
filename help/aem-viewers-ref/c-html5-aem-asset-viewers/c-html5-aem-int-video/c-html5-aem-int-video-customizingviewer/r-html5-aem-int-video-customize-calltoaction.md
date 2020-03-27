---
description: El panel Llamada a acción aparece cuando termina el vídeo y muestra todas las muestras interactivas asociadas al vídeo en particular.
seo-description: El panel Llamada a acción aparece cuando termina el vídeo y muestra todas las muestras interactivas asociadas al vídeo en particular.
seo-title: Llamada a acción
solution: Experience Manager
title: Llamada a acción
topic: Dynamic media
uuid: 04a042d8-7329-4f1d-b3b9-312d620b1f29
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Llamada a acción{#call-to-action}

El panel Llamada a acción aparece cuando termina el vídeo y muestra todas las muestras interactivas asociadas al vídeo en particular.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El panel consta de un área de encabezado que muestra el título del vídeo, un botón de reproducción en la esquina superior derecha y muestras interactivas reales que se muestran como una cuadrícula desplazable. Puede deshabilitar el panel mediante el atributo de configuración [callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6) .

El panel de llamada a acción siempre ocupa toda el área del visor disponible.

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

El siguiente selector de clase CSS controla el aspecto del color de fondo en el panel de llamada a acción:

```
.s7interactivevideoviewer .s7calltoaction
```

## Propiedades CSS del color de fondo del panel de llamada a acción {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo del panel de llamada a acción. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#example}

Para configurar un panel de llamada a acción con fondo gris oscuro:

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

El siguiente selector de clase CSS controla el aspecto del encabezado en el panel de llamada a acción:

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## Propiedades CSS del encabezado del panel de llamada a acción {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del encabezado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del encabezado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom </span> </p> </td> 
   <td colname="col2"> <p>Borde inferior del encabezado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#example-1}

Para configurar un encabezado de 70 píxeles de alto, con un fondo gris oscuro y un borde de dos píxeles más claro a lo largo de la parte inferior:

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

El siguiente selector de clase CSS controla el aspecto del título del encabezado en el panel de llamada a acción:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## Propiedades CSS del título del encabezado en el panel de llamada a acción:  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Color del texto dentro del letrero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Altura de línea. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Familia de fuentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Alineación del texto en la pancarta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno-izquierda </span> </p> </td> 
   <td colname="col2"> <p>Relleno izquierdo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno-derecha </span> </p> </td> 
   <td colname="col2"> <p> Relleno derecho para permitir espacio para el botón Reproducir. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#example-2}

Para configurar un título de vídeo con una altura de línea de 70 píxeles, un tamaño de fuente de 25 píxeles, color blanco y alineación a la izquierda:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

El siguiente selector de clase CSS controla el aspecto del botón de cierre en el panel de llamada a acción:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## Propiedades CSS del botón de cierre del panel de llamada a acción: {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la parte superior del encabezado, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la derecha del encabezado, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Imagen mostrada para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Colocar dentro del elemento sprite de ilustración, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de `state` atributos, que se puede utilizar para aplicar diferentes apariencias a diferentes estados de botón.

## Ejemplo {#example-3}

Para configurar un botón de reproducción de 28 x 28 píxeles; colocado 20 píxeles desde la parte superior y desde el borde derecho del encabezado; muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes; toma la ilustración de la imagen de Sprite del componente:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

El siguiente selector de clase CSS controla el aspecto de la vista de cuadrícula de miniaturas en el panel de llamada a acción:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## Propiedades CSS de la vista de cuadrícula de miniaturas en el panel de llamada a acción:  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del área de miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#example-4}

Para configurar un área de miniaturas con un fondo gris oscuro:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

El siguiente selector de clase CSS controla el aspecto de la celda de la miniatura en el panel de llamada a acción:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## Propiedades CSS de la celda miniatura en el panel de llamada a acción: {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Tamaño del margen horizontal y vertical alrededor de cada miniatura. </p> <p>El espaciado de las miniaturas horizontales es igual a la suma de los márgenes izquierdo y derecho definidos para <span class="codeph"> .s7thumbcell </span>. La misma regla también se aplica, pero al espaciado vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#example-5}

Para configurar el espaciado horizontal de 24 píxeles y el espaciado vertical de 18 píxeles:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

El siguiente selector de clase CSS controla el aspecto de la miniatura en el panel de llamada a acción:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## Propiedades CSS de la miniatura en el panel de llamada a acción: {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde de la miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura admite el selector de `state` atributos, que se puede utilizar para aplicar diferentes apariencias a distintos estados de miniaturas. En particular, `state="selected"` corresponde a la miniatura de la imagen seleccionada actualmente; `state="default"` corresponde al resto de miniaturas; `state="over"` se utiliza al pasar el ratón por encima.

## Ejemplo {#example-6}

Para configurar miniaturas de 94 x 100 píxeles:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

El siguiente selector de clase CSS controla el aspecto de la etiqueta de miniatura en el panel de llamada a acción:

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## Propiedades CSS de la etiqueta de miniatura en el panel de llamada a acción: {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Color del texto de la etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Alineación horizontal de la etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nombre de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#example-7}

Para configurar etiquetas que utilicen un color blanco, alinee el centro 15 píxeles y utilice una fuente Arial:

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

Si hay más miniaturas de las que se pueden ajustar verticalmente a la vista, las miniaturas representan una barra de desplazamiento vertical en el lado derecho. De forma predeterminada, el panel de llamada a acción procesa una pequeña barra vertical sin botones de desplazamiento ni de desplazamiento. Sin embargo, es posible personalizar la barra modificando la CSS del visor.

El siguiente selector de clase CSS controla el aspecto del área de la barra de desplazamiento en el panel de llamada a acción:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## Propiedades CSS del área de la barra de desplazamiento del panel de llamada a acción: {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho de la barra de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Desplazamiento de la barra de desplazamiento vertical desde la parte superior del área de miniaturas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Desplazamiento de la barra de desplazamiento vertical desde la parte inferior del área de miniaturas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento de la barra de desplazamiento horizontal desde el borde derecho del área de miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#example-8}

Para configurar una barra de desplazamiento con una anchura de 22 píxeles y sin ningún margen en la parte superior, derecha o inferior del área de miniaturas:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

La pista de la barra de desplazamiento es el área entre los botones de la barra de desplazamiento superior e inferior. El componente establece automáticamente la posición y la altura de la pista.

El siguiente selector de clase CSS controla el aspecto de la pista de la barra de desplazamiento en el panel de llamada a acción:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## Propiedades CSS de la barra de seguimiento de desplazamiento {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho de la barra de seguimiento de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo de la barra de seguimiento. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#example-9}

Para configurar una pista de barra de desplazamiento con una anchura de 22 píxeles y un color gris:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

El pulgar de la barra de desplazamiento se mueve verticalmente dentro del área de la pista de desplazamiento. Su posición vertical está totalmente controlada por la lógica del componente; sin embargo, la altura de la miniatura no cambia dinámicamente según la cantidad de contenido.

El siguiente selector de clase CSS controla el aspecto de la altura del pulgar y otros aspectos:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## Propiedades CSS de la altura de la miniatura en el panel de llamada a acción: {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del pulgar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del pulgar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>Relleno vertical entre la parte superior de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno-inferior </span> </p> </td> 
   <td colname="col2"> <p>Relleno vertical entre la parte inferior de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Radio del borde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color del pulgar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Imagen mostrada para un estado de pulgar determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb admite el selector de `state` atributos, que se puede utilizar para aplicar diferentes apariencias a los siguientes estados de dedo: `"up"`, `"down"`, `"over"`y `"disabled"`.

## Ejemplo {#example-10}

Para configurar una miniatura de la barra de desplazamiento de 6 x 167 píxeles, tiene tres esquinas redondeadas de píxeles y un color gris:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

El siguiente selector de clase CSS controla el aspecto de los botones de desplazamiento superior e inferior:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

No es posible colocar botones de desplazamiento mediante las propiedades CSS top, left, bottom o right; la lógica del visor las coloca automáticamente. El panel de llamada a acción del visor de vídeo interactivo no utiliza estos botones en la barra de desplazamiento, por lo que su tamaño se establece en 0 píxeles en el CSS predeterminado.

## Propiedades CSS de los botones de desplazamiento superior e inferior del panel de llamada a acción:  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Imagen mostrada para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Estos botones admiten el selector de `state` atributos, que se puede utilizar para aplicar diferentes apariencias a los siguientes estados de dedo: `"up"`, `"down"`, `"over"`y `"disabled"`.

La información del objeto de botón se puede localizar. Consulte [Localización de los elementos](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)de la interfaz de usuario.

## Ejemplo {#example-11}

Desactive los botones de desplazamiento estableciendo su tamaño en 0 y ocultándolos:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```

