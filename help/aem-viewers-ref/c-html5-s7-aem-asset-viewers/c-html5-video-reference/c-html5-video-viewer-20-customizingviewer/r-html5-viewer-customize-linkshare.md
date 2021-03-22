---
description: La herramienta Compartir vínculos consiste en un botón agregado al panel Compartir en Social y el cuadro de diálogo modal que se muestra cuando se activa la herramienta. La posición del botón la gestiona completamente la herramienta de uso compartido de Social.
seo-description: La herramienta Compartir vínculos consiste en un botón agregado al panel Compartir en Social y el cuadro de diálogo modal que se muestra cuando se activa la herramienta. La posición del botón la gestiona completamente la herramienta de uso compartido de Social.
seo-title: Compartir vínculos
solution: Experience Manager
title: Compartir vínculos
uuid: 699ddab2-8cfd-4edf-bb1b-5ff91fe63c1a
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1425'
ht-degree: 2%

---


# Compartir vínculos{#link-share}

La herramienta Compartir vínculos consiste en un botón agregado al panel Compartir en Social y el cuadro de diálogo modal que se muestra cuando se activa la herramienta. La posición del botón la gestiona completamente la herramienta de uso compartido de Social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

El aspecto del botón para compartir vínculos se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkshare
```

**Propiedades CSS de la herramienta para compartir vínculos**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

Es posible quitar el botón del panel Compartir en Social estableciendo la propiedad `display:none` CSS en su clase CSS.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar un botón de compartir vínculos de 28 x 28 píxeles y mostrar una imagen diferente para cada uno de los cuatro estados de botones diferentes:

```
.s7videoviewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7videoviewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7videoviewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7videoviewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

La superposición de fondo que cubre la página web cuando el cuadro de diálogo está activo se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7backoverlay
```

**Propiedades CSS de la superposición de fondo**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidad  </span> </p> </td> 
   <td colname="col2"> <p>Opacidad de la superposición de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de superposición de fondo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una superposición de fondo para que sea gris con un 70 % de opacidad:

```
.s7videoviewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

De forma predeterminada, el cuadro de diálogo modal se muestra centrado en la pantalla de los sistemas de escritorio y toma todo el área de la página web en dispositivos táctiles. En todos los casos, el componente gestiona la colocación y el tamaño del cuadro de diálogo. El cuadro de diálogo se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7dialog
```

**Propiedades CSS del cuadro de diálogo**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Radio del borde del cuadro de diálogo, en caso de que el cuadro de diálogo no tome todo el explorador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del cuadro de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Debe estar desconfigurado o estar configurado al 100%, en cuyo caso el cuadro de diálogo toma toda la ventana del explorador (este modo se prefiere en los dispositivos táctiles). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Debe estar desconfigurado o estar configurado al 100%, en cuyo caso el cuadro de diálogo toma toda la ventana del explorador (este modo se prefiere en los dispositivos táctiles). </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Configurar el cuadro de diálogo para que utilice toda la ventana del explorador y tenga un fondo blanco en dispositivos táctiles:

```
.s7videoviewer .s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

El encabezado del cuadro de diálogo consiste en un icono, un texto de título y un botón de cierre. El contenedor de encabezado está controlado con

```
.s7videoviewer .s7linkdialog .s7dialogheader
```

**Propiedades CSS del encabezado del cuadro de diálogo**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Margen interior para el contenido del encabezado. </p> </td> 
  </tr> 
 </tbody> 
</table>

El icono y el texto del título se envuelven en un contenedor adicional controlado con

```
.s7videoviewer .s7linkdialog .s7dialogheader .s7dialogline
```

**Propiedades CSS de la línea de diálogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Margen interior para el icono y el título del encabezado </p> </td> 
  </tr> 
 </tbody> 
</table>

El icono de encabezado se controla con el siguiente selector de clase CSS

```
.s7videoviewer .s7linkdialog .s7dialogheadericon
```

**Propiedades CSS del icono de encabezado del cuadro de diálogo**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p>Icono imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

El título del encabezado se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7dialogheadertext
```

**Propiedades CSS del texto del encabezado del cuadro de diálogo**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Altura de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen de texto interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

El botón Cerrar se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7closebutton
```

**Propiedades CSS del botón de cierre **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p> Posición vertical del botón con respecto al contenedor de encabezado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p> Posición horizontal del botón en relación con el contenedor de encabezado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen interior del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p>Imagen de botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

La información del objeto del botón Cerrar y el título del cuadro de diálogo se pueden localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar un encabezado de cuadro de diálogo con relleno, un icono de 22 x 12 píxeles, un título en negrita de 16 puntos y un botón Cerrar de 28 x 28 píxeles que se sitúe a dos píxeles de la parte superior y a dos píxeles de la derecha del contenedor de cuadro de diálogo:

```
.s7videoviewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

El pie de página del cuadro de diálogo consiste en el botón &quot;cancelar&quot;. El contenedor de pie de página se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7dialogfooter
```

**Propiedades CSS del pie de página del cuadro de diálogo **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p> Borde que puede utilizar para separar visualmente el pie de página del resto del cuadro de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El pie de página tiene un contenedor interior que mantiene el botón . Se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7dialogbuttoncontainer
```

**Propiedades CSS del contenedor de botones de cuadro de diálogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Margen interior entre el pie de página y el botón. </p> </td> 
  </tr> 
 </tbody> 
</table>

El botón Seleccionar todo está controlado con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7dialogactionbutton
```

El botón solo está disponible en sistemas de escritorio.

**Propiedades CSS del botón Seleccionar todo**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Color del texto del botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo de botón para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El botón Seleccionar todo admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

El botón Cancelar se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7dialogcancelbutton
```

**Propiedades CSS del botón Cancelar del cuadro de diálogo**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Color del texto del botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo de botón para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

Además, ambos botones comparten la misma clase CSS común que puede contener ajustes CSS que son los mismos para otros botones del cuadro de diálogo:

```
.s7videoviewer .s7linkdialog .s7dialogfooter .s7button
```

**Propiedades CSS del botón**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Grosor de la fuente del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p> Altura del texto dentro del botón. Afecta a la alineación vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-Shadow  </span> </p> </td> 
   <td colname="col2"> <p>Sombra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right  </span> </p> </td> 
   <td colname="col2"> <p>Margen del botón derecho. </p> </td> 
  </tr> 
 </tbody> 
</table>

La información sobre herramientas de botones se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar un pie de página de un cuadro de diálogo con un botón Cancelar de 64 x 34, con un color de texto y de fondo diferentes para cada estado de botón:

```
.s7videoviewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

El área de diálogo principal (entre el encabezado y el pie de página) contiene contenido de cuadro de diálogo. En todos los casos, el componente gestiona la anchura de esta área; no es posible configurarla en CSS. El área de diálogo principal se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7dialogviewarea
```

**Propiedades CSS del área de visualización del cuadro de diálogo **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Altura del área principal del cuadro de diálogo. Solo debe especificarse cuando el cuadro de diálogo funciona en modo de escritorio. No es aplicable cuando el cuadro de diálogo tiene el tamaño necesario para ocupar toda la ventana del explorador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del área del cuadro de diálogo principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Margen exterior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un área del cuadro de diálogo principal con una altura de 300 píxeles, tener un margen de diez píxeles y usar un fondo blanco:

```
.s7videoviewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Todo el contenido del formulario (como etiquetas y campos de entrada) reside dentro de un contenedor controlado con

```
.s7videoviewer .s7linkdialog .s7dialogbody
```

**Propiedades CSS del cuerpo del cuadro de diálogo **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Configurar el contenido del formulario para que tenga un relleno de diez píxeles:

```
.s7videoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

Todas las etiquetas estáticas del formulario del cuadro de diálogo se controlan con

```
.s7videoviewer .s7linkdialog .s7dialoglabel
```

Esta clase no es adecuada para controlar el tamaño o la posición de la etiqueta porque puede aplicarla a textos en varios lugares de la interfaz de usuario del formulario.

**Propiedades CSS de la etiqueta del cuadro de diálogo. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente de la etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente de la etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes de etiquetas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Color del texto de la etiqueta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Las etiquetas del cuadro de diálogo se pueden localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar todas las etiquetas para que sean grises, negrita con una fuente de nueve píxeles:

```
.s7videoviewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

El tamaño de la copia de texto mostrada sobre el vínculo se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7dialoginputwide
```

**Propiedades CSS del campo ancho de entrada del cuadro de diálogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Anchura del texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para definir la copia de texto en 430 píxeles de ancho y con un relleno de diez píxeles en la parte inferior:

```
.s7videoviewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

El vínculo compartido se envuelve en un contenedor y se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7dialoginputcontainer
```

**Propiedades CSS del contenedor de entrada del cuadro de diálogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde alrededor del contenedor de vínculos compartidos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para definir un borde gris de un píxel alrededor del texto del código incrustado y tener nueve píxeles de relleno:

```
.s7videoviewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

El vínculo compartido en sí se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7linkdialog .s7dialoglink
```

**Propiedades CSS del vínculo de uso compartido del cuadro de diálogo**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Compartir la anchura del vínculo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para establecer el vínculo compartido en 450 píxeles de ancho:

```
.s7videoviewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```

