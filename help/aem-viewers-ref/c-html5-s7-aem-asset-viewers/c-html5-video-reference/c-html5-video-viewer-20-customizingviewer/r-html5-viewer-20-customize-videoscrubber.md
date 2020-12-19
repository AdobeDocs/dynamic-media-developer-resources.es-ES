---
description: La barra de desplazamiento de vídeo es el control deslizante horizontal que permite al usuario buscar dinámicamente cualquier posición temporal dentro del vídeo que se está reproduciendo.
seo-description: La barra de desplazamiento de vídeo es el control deslizante horizontal que permite al usuario buscar dinámicamente cualquier posición temporal dentro del vídeo que se está reproduciendo.
seo-title: Borrador de vídeo
solution: Experience Manager
title: Borrador de vídeo
topic: Dynamic media
uuid: 5e4abc8a-ee61-4528-a5de-66148aac3389
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 2%

---


# Barra de desplazamiento de vídeo{#video-scrubber}

La barra de desplazamiento de vídeo es el control deslizante horizontal que permite al usuario buscar dinámicamente cualquier posición temporal dentro del vídeo que se está reproduciendo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El control &#39;knob&#39; de la barra de desplazamiento también se mueve a medida que se reproduce el vídeo para indicar la posición de tiempo actual del vídeo durante la reproducción. La barra de desplazamiento de vídeo siempre toma toda la anchura de la barra de control. Es posible deslizar la barra de desplazamiento del vídeo. cambie la altura y la posición vertical mediante CSS.

El aspecto general de la barra de desplazamiento de vídeo se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**Propiedades CSS de la barra de desplazamiento de vídeo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde superior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p> Posición desde el borde inferior, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de la barra de desplazamiento del vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de la barra de desplazamiento del vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Los siguientes selectores de clase CSS rastrean indicadores de fondo, reproducción y carga:

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**Propiedades CSS del seguimiento**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura de la pista correspondiente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de la pista correspondiente. </p> </td> 
  </tr> 
 </tbody> 
</table>

El siguiente selector de clase CSS controla el control:

```
.s7videoviewer .s7videoscrubber .s7knob
```

**Propiedades CSS del botón**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Desplazamiento vertical del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del pomo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del pomo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Ilustración del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

El siguiente selector de clase CSS controla el tiempo de reproducción de la burbuja:

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**Propiedades CSS de la burbuja de tiempo de reproducción**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> Familia de fuentes que se va a utilizar para mostrar el texto durante el tiempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> El tamaño de fuente que se va a utilizar para mostrar el texto durante el tiempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> El color de fuente que se usará para mostrar el texto durante el tiempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del área de burbujas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del área de burbujas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno del área de burbujas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Ilustración de burbujas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>Alineación del texto con el área de la burbuja. </p> </td> 
  </tr> 
 </tbody> 
</table>

La información de la herramienta de limpieza de vídeo se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

**Ejemplo** : Para configurar un visor de vídeo con una barra de desplazamiento de vídeo con colores de pista personalizados de 10 píxeles de altura y colocados 10 píxeles y 35 píxeles desde los bordes superior e izquierdo de la barra de control.

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

Cuando se habilita el capítulo de vídeo con el parámetro `navigation`, las ubicaciones de capítulo se muestran como marcadores en la parte superior de la pista de desplazamiento de vídeo.

El marcador de capítulo de vídeo está controlado por el siguiente selector de clase CSS:

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

**Propiedades CSS del marcador de capítulo de vídeo**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del marcador de capítulos de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del marcador de capítulos de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Ilustración del marcador de capítulos de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizar para aplicar diferentes apariencias a distintos estados de botones. En particular, `selected='default'` corresponde al estado del marcador de capítulo de vídeo predeterminado y `selected='over'` se utiliza cuando el marcador de capítulo de vídeo se activa mediante un gesto de toque o de desplazamiento del ratón.

**Ejemplo** : para configurar un marcador de capítulo de vídeo de 5 x 8 píxeles y utilizar una ilustración diferente para los estados &quot;predeterminado&quot; y &quot;sobre&quot;.

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

La burbuja de capítulos de vídeo se sitúa sobre el marcador de capítulos de vídeo y muestra el título, la hora de inicio y la descripción de un capítulo determinado. Es posible controlar la anchura máxima de la burbuja y el desplazamiento vertical en relación con la pista de la barra de desplazamiento del vídeo. El resto lo calcula automáticamente el componente.

La burbuja de capítulos de vídeo está controlada por el siguiente selector de clases CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**Propiedades CSS de la burbuja de capítulos de vídeo**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho máximo de la burbuja de capítulos de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Desplazamiento vertical de la pista de desplazamiento de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** : para configurar una burbuja de capítulos de vídeo de 235 píxeles de ancho y ocho píxeles de alto desde la parte inferior de la pista de desplazamiento de vídeo.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

La burbuja de capítulos de vídeo consta de un encabezado y contenido opcionales. El encabezado tiene el tiempo de inicio opcional del capítulo y el título del capítulo.

El encabezado está controlado por el siguiente selector de clase CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**Propiedades CSS del encabezado de burbuja de capítulos de vídeo**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del encabezado de la burbuja de capítulos de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior para texto de encabezado de burbujas de capítulos de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del encabezado de burbuja de capítulos de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p>Altura de la línea de texto del encabezado de la burbuja de capítulos de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** : para configurar un encabezado de burbuja de capítulos de vídeo con una altura de 22 píxeles, una altura de línea de 22 píxeles, un margen horizontal de 12 píxeles y un fondo gris.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

El tiempo de inicio del capítulo de vídeo se controla mediante el siguiente selector de clase CSS:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**Propiedades CSS del tiempo de inicio del capítulo de vídeo**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Color de texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p>Peso de fuentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno-derecha  </span> </p> </td> 
   <td colname="col2"> <p> Relleno entre el tiempo de inicio y el título del capítulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** : para configurar el tiempo de inicio del capítulo con una fuente Verdana gris de diez píxeles y con un margen de diez píxeles a la derecha.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

El título del capítulo de vídeo está controlado por el siguiente selector de clase CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**Propiedades CSS del título del capítulo de vídeo**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Color del texto del título del capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p>Peso de fuente del título del capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente del título del capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes del título del capítulo de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** : para configurar un título de capítulo de vídeo que utilice una fuente Verdana de diez píxeles en blanco, negrita y negrita.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

La descripción del capítulo de vídeo está controlada por el siguiente selector de clase CSS:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

**Propiedades CSS de la descripción del capítulo de vídeo**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Color de texto de descripción del capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo de descripción del capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p>Peso de fuentes de descripción de capítulos de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente de descripción del capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Descripción de la familia de fuentes del capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p>Alto de línea de descripción del capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Descripción del relleno interior del capítulo de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** : para configurar la descripción de capítulos de vídeo con una fuente Verdana de 11 píxeles y gris oscuro con un fondo gris claro; 5 píxeles de altura de línea, 12 píxeles de margen horizontal, 12 píxeles de relleno superior y 9 píxeles de relleno inferior.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

El conector de cuña situado en la parte inferior de la burbuja de capítulos está controlado por el siguiente selector de clase CSS:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**Propiedades CSS del conector de cuña**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color  </span> </p> </td> 
   <td colname="col2"> <p>Color del conector de arista. </p> <p>Definido como <span class="codeph"> &lt;color&gt; transparente </span> de modo que sólo se defina el color del borde superior y los bordes restantes se dejen transparentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width  </span> </p> </td> 
   <td colname="col2"> <p> Anchura del conector Wedge. </p> <p>Definido como <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> de manera que la misma anchura se defina sólo para los bordes superior y horizontal y la anchura del borde inferior sea <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Define un margen inferior negativo solamente. Debe tener el mismo valor que el de <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** : para configurar un conector de seis píxeles de cuña gris:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

