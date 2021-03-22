---
description: El panel Muestras interactivas aparece junto al contenido del vídeo si se han pasado datos interactivos al visor en la configuración. Consiste en un banner en la parte superior que representa texto como "Haga clic para ver", una columna de uno o más muestras interactivas y dos botones de desplazamiento (disponibles solo en sistemas de escritorio).
seo-description: El panel Muestras interactivas aparece junto al contenido del vídeo si se han pasado datos interactivos al visor en la configuración. Consiste en un banner en la parte superior que representa texto como "Haga clic para ver", una columna de uno o más muestras interactivas y dos botones de desplazamiento (disponibles solo en sistemas de escritorio).
seo-title: Muestras interactivas
solution: Experience Manager
title: Muestras interactivas
uuid: 9f9df764-3dd0-414e-a0db-4287f0019313
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 2%

---


# Muestras interactivas{#interactive-swatches}

El panel Muestras interactivas aparece junto al contenido del vídeo si se han pasado datos interactivos al visor en la configuración. Consiste en un banner en la parte superior que representa texto como &quot;Haga clic para ver&quot;, una columna de uno o más muestras interactivas y dos botones de desplazamiento (disponibles solo en sistemas de escritorio).

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

En sistemas de escritorio y en dispositivos táctiles, en orientación horizontal, los muestras interactivas se representan verticalmente a la derecha del contenido de vídeo. En dispositivos táctiles en orientación vertical, aparecen en la parte inferior del visor como una fila horizontal de muestras.

El selector de clase CSS siguiente controla la ubicación y la orientación del panel de muestras interactivo:

```
.s7interactivevideoviewer .s7interactiveswatches
```

## Propiedades CSS de las muestras interactivas {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del panel de muestras interactivo </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del panel de muestras interactivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Posición superior del panel de muestras interactivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición inferior del panel de muestras interactivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> izquierda </span> </p> </td> 
   <td colname="col2"> <p>Posición izquierda del panel de muestras interactivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p>Posición derecha del panel de muestras interactivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

La ubicación y orientación en tiempo de ejecución del panel de muestras interactivas se definen mediante una combinación de las propiedades CSS anteriores de la siguiente manera:

* Para representar muestras interactivas horizontalmente en la parte inferior del visor, establezca la altura en un valor de píxel absoluto; izquierda y abajo a 0px; ancho, derecho y superior a automático.
* Para procesar muestras interactivas verticalmente a la derecha del contenido de vídeo, defina la anchura en un píxel absoluto; derecha y arriba a 0px; altura, izquierda e inferior para auto.

Es posible utilizar marcadores CSS junto con este estilo para lograr la ubicación adaptativa del panel de muestras interactivo.

## Ejemplo {#example}

Para configurar un panel de muestras interactivo para que se represente horizontalmente en la parte inferior del visor en dispositivos táctiles en orientación horizontal y para que se muestre verticalmente a la derecha del contenido de vídeo en todos los demás casos:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El tamaño y la posición del banner lo gestiona el componente de muestras interactivas basado en otro estilo aplicado con CSS y no se puede establecer explícitamente.

El siguiente selector de clase CSS controla el aspecto del panel del banner:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## Propiedades CSS del panel del banner {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del panel del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color del texto dentro del panel del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde alrededor del panel del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Peso de la fuente que se utilizará para el texto dentro del panel del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>El tamaño de fuente que se utilizará para el texto dentro del panel del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>La familia de fuentes que se utilizará para el texto dentro del panel del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>Alineación de fuente que se utilizará para el texto dentro del panel del banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

La información del objeto del banner se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

## Ejemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar un banner con fondo gris oscuro, borde más claro de dos píxeles y el texto blanco centrado horizontalmente:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

El siguiente selector de clase CSS controla el aspecto de las muestras:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## Propiedades CSS del área de muestras {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del área de muestras. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-9cadd62a09fd44a280f55ff42437e416}

Para configurar el área de muestras con fondo gris oscuro:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

El siguiente selector de clase CSS controla el espaciado entre miniaturas de muestra:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## Propiedades CSS del espaciado de las miniaturas de las muestras {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> El tamaño del margen horizontal y vertical alrededor de cada miniatura. El espaciado en miniatura real es igual a la suma de los márgenes izquierdo y derecho establecidos para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-39fb270b7e494a9d99e6e8f6890ec53c}

Para configurar el espaciado vertical para que sea de 10 píxeles:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

El siguiente selector de clase CSS controla el aspecto de las miniaturas individuales:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## Propiedades CSS del aspecto de miniaturas individuales {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
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

>[!NOTE]
>
>La miniatura admite el selector de atributos `state`, que puede utilizar para aplicar diferentes aspectos a distintos estados de miniaturas. En concreto, `state="selected"` corresponde a la miniatura de la imagen seleccionada actualmente; `state="default"` corresponde al resto de miniaturas; `state="over"` se utiliza al pasar el ratón por encima.

## Ejemplo {#section-69fec189ffaa440b97b6b846c320b75b}

Para configurar miniaturas de 100 x 75 píxeles:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

El selector de clase CSS siguiente controla el aspecto de la etiqueta de miniatura:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## Propiedades CSS del aspecto de la etiqueta de miniatura {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Color de texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde de la etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>Alineación de texto horizontal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nombre de la fuente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-eb141eb6c1154183baa69796edb90536}

Para configurar etiquetas para que utilicen alineación a la izquierda, blanco, 12 píxeles, fuente Helvetica y un borde inferior:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

El selector de clase CSS siguiente controla el aspecto de los botones de desplazamiento hacia arriba y hacia abajo:

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

No es posible colocar los botones de desplazamiento utilizando las propiedades CSS `top`, `left`, `bottom` y `right`; en su lugar, la lógica del visor los coloca automáticamente.

## Propiedades CSS del aspecto de los botones de desplazamiento hacia arriba y hacia abajo {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Anchura del botón de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p>Posición dentro del sprite de ilustración, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizar para aplicar diferentes aspectos a los estados de botones: &quot; `up`&quot;, &quot; `down`&quot;, &quot; `over`&quot; y &quot; `disabled`&quot;.

La información sobre herramientas de botones se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

## Ejemplo {#section-e6ce4fa084b84288bc7583342b2c510c}

Para configurar el botón de desplazamiento hacia arriba que sea de 60 x 36 píxeles, tenga distintas ilustraciones para cada estado y tome esa ilustración de la imagen Sprite del componente:

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```

