---
description: El control de volumen mutable aparece inicialmente como un botón que permite al usuario silenciar o anular el silencio del sonido del reproductor de vídeo.
seo-description: El control de volumen mutable aparece inicialmente como un botón que permite al usuario silenciar o anular el silencio del sonido del reproductor de vídeo.
seo-title: Volumen mutable
solution: Experience Manager
title: Volumen mutable
topic: Dynamic media
uuid: d7eafff8-dd98-42e2-9d45-e291fe372d8c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 2%

---


# Volumen mutable{#mutable-volume}

El control de volumen mutable aparece inicialmente como un botón que permite al usuario silenciar o anular el silencio del sonido del reproductor de vídeo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Cuando un usuario pasa el ratón sobre el botón, aparece un deslizador que permite al usuario configurar el volumen. El control de volumen mutable se puede cambiar de tamaño, de piel y de posición, en relación con la barra de control que lo contiene, mediante CSS.

El aspecto del área de volumen mutable se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7mutablevolume
```

**Propiedades CSS del volumen mutable**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p> Posición desde el borde superior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p> Posición desde el borde derecho, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho del control de volumen mutable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del control de volumen mutable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color del control de volumen mutable. </p> </td> 
  </tr> 
 </tbody> 
</table>

El aspecto del botón silenciar/anular el silencio se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7mutablevolume .s7mutebutton
```

Puede controlar la imagen de fondo para cada estado del botón. El tamaño del botón se hereda del tamaño del control de volumen.

**Propiedades CSS de la imagen del botón**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite los selectores de atributos `state` y `selected`, que pueden utilizarse para aplicar diferentes apariencias a diferentes estados de botón. En particular, `selected='true'` corresponde al estado &quot;silenciado&quot; y `selected='false'` corresponde al estado &quot;no silenciado&quot;.

El área de la barra de volumen vertical se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume
```

**Propiedades CSS del área de la barra de volumen vertical**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo del volumen vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Ancho del volumen vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Altura del volumen vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

La pista dentro del control de volumen vertical se controla con los siguientes selectores de clase CSS:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**Propiedades CSS del control de volumen vertical**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo del control de volumen vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del control de volumen vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del control de volumen vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

El control de volumen vertical se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**Propiedades CSS del control de volumen vertical**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Ilustración del pomo de control de volumen vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del pomo de control vertical del volumen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del pomo de control de volumen vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> izquierda </span> </p> </td> 
   <td colname="col2"> <p>Posición horizontal del pomo de control vertical del volumen. </p> </td> 
  </tr> 
 </tbody> 
</table>

La información de objeto del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

## Ejemplos {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar un botón de silencio de 32 x 32 píxeles y posicionado 6 píxeles desde la parte superior y 38 píxeles desde el borde derecho de la barra de control. Muestre una imagen diferente para cada uno de los cuatro estados de botón diferentes cuando esté seleccionado o no.

```
.s7videoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

A continuación se muestra un ejemplo de cómo puede aplicar estilo al control deslizante del volumen dentro del control de volumen mutable.

```
.s7videoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```

A continuación se muestra un ejemplo de cómo puede personalizar el reproductor de vídeo para que el sonido se desactive durante la reproducción. Añada el siguiente código al código incrustado del visor:

```
                "handlers":{ 
                    "initComplete":function() { 
                        videoViewer.getComponent("mutableVolume").setPosition(0); 
                        videoViewer.getComponent("mutableVolume").deactivate(); 
                    } 
                }
```

En el ejemplo de código anterior, el nivel de volumen se establece en `0` en el componente `mutableVolume`. A continuación, se desactiva el mismo componente para que el usuario final no pueda utilizarlo.
