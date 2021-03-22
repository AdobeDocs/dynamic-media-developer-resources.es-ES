---
description: La herramienta Insertar uso compartido consiste en un botón añadido al panel Compartir en Social y el cuadro de diálogo modal que se muestra cuando se activa la herramienta. La posición del botón la gestiona completamente la herramienta de uso compartido de Social .
seo-description: La herramienta Insertar uso compartido consiste en un botón añadido al panel Compartir en Social y el cuadro de diálogo modal que se muestra cuando se activa la herramienta. La posición del botón la gestiona completamente la herramienta de uso compartido de Social .
seo-title: Incrustar recurso compartido
solution: Experience Manager
title: Incrustar recurso compartido
uuid: 59a21a90-5f34-4e1f-90e7-cce18aed5e6b
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2650'
ht-degree: 2%

---


# Incrustar recurso compartido{#embed-share}

La herramienta Insertar uso compartido consiste en un botón añadido al panel Compartir en Social y el cuadro de diálogo modal que se muestra cuando se activa la herramienta. La posición del botón la gestiona completamente la herramienta de uso compartido de Social .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del botón de incrustación compartida se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embedshare
```

**Propiedades CSS de la herramienta de uso compartido incrustado**

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
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

Es posible quitar el botón del panel Compartir en Social estableciendo la propiedad `display:none` CSS en su clase CSS.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: para configurar un botón de incrustación compartida de 28 x 28 píxeles y muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes:

```
.s7ecatalogviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7ecatalogviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7ecatalogviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7ecatalogviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

La superposición de fondo que cubre la página web cuando el cuadro de diálogo está activo se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7backoverlay
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
.s7ecatalogviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

De forma predeterminada, el cuadro de diálogo modal se muestra centrado en la pantalla de los sistemas de escritorio y toma todo el área de la página web en dispositivos táctiles. En todos los casos, el componente gestiona la colocación y el tamaño del cuadro de diálogo. El cuadro de diálogo se controla con el siguiente selector de clase CSS:

```
.s7embeddialog .s7dialog
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
.s7ecatalogviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

El encabezado del cuadro de diálogo consiste en un icono, un texto de título y un botón de cierre. El contenedor de encabezado está controlado con

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader
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
.s7ecatalogviewer .s7embeddialog .s7dialogheader .s7dialogline
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
.s7ecatalogviewer .s7embeddialog .s7dialogheadericon
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
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

El título del encabezado se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogheadertext
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
.s7ecatalogviewer .s7embeddialog .s7closebutton
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
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: para configurar el encabezado del cuadro de diálogo con relleno, el icono de 24 x 14 píxeles, el título en negrita de 16 puntos y el botón de cierre de 28 x 28 píxeles, colocado dos píxeles desde la parte superior y dos píxeles desde la parte derecha del contenedor de cuadro de diálogo:

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

El pie de página del cuadro de diálogo consiste en el botón &quot;cancelar&quot;. El contenedor de pie de página se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter
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
.s7ecatalogviewer .s7embeddialog .s7dialogbuttoncontainer
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
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton
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
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton
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
.s7ecatalogviewer .s7embeddialog .s7dialogfooter .s7button
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

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: para configurar un pie de página de cuadro de diálogo con un botón Cancelar de 64 x 34, un botón Seleccionar todo de 82 x 34 y con un color de texto y de fondo diferentes para cada estado de botón:

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

El área de diálogo principal (entre el encabezado y el pie de página) contiene el contenido del cuadro de diálogo desplazable y el panel de desplazamiento de la derecha. En todos los casos, el componente administra la anchura de esta área, no es posible configurarla en CSS. El área de diálogo principal se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogviewarea
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
.s7ecatalogviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Todo el contenido del formulario (como etiquetas y campos de entrada) reside dentro de un contenedor controlado con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogbody
```

Si la altura de este contenedor parece ser mayor que el área del cuadro de diálogo principal, el componente activa automáticamente un desplazamiento vertical.

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
.s7ecatalogviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Todas las etiquetas estáticas del formulario del cuadro de diálogo se controlan con

```
.s7ecatalogviewer .s7embeddialog .s7dialoglabel
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

Las etiquetas de los cuadros de diálogo se pueden localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: para configurar todas las etiquetas para que sean grises, negrita con una fuente de nueve píxeles:

```
.s7ecatalogviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

El tamaño de la copia de texto mostrada sobre el código incrustado se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputwide
```

**Propiedades CSS del campo ancho de entrada del cuadro de diálogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para definir la copia de texto en 430 píxeles de ancho y con un relleno de diez píxeles en la parte inferior:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

El código incrustado se coloca dentro del contenedor y se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer
```

**Propiedades CSS del contenedor de entrada del cuadro de diálogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del contenedor de código incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde alrededor del contenedor de código incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para definir un borde gris de un píxel alrededor del texto del código incrustado, marque 430 píxeles de ancho y tenga un relleno de diez píxeles:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

El texto del código incrustado real se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer
```

**Propiedades CSS del contenedor de entrada del cuadro de diálogo**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ajuste de palabras  </span> </p> </td> 
   <td colname="col2"> <p>Estilo de ajuste de palabras. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar el código incrustado para utilizar `break-word` ajuste de palabras:

```
.s7ecatalogviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

La etiqueta de tamaño de incrustación y la lista desplegable se encuentran en la parte inferior del cuadro de diálogo y se incluyen en un contenedor controlado con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel
```

**Propiedades CSS del panel Tamaño incrustado del cuadro de diálogo**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un panel de tamaño incrustado de modo que tenga diez píxeles de relleno:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

El tamaño y la alineación de la etiqueta de tamaño incrustado se controlan con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel
```

**Propiedades CSS del panel Tamaño incrustado del cuadro de diálogo**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alineación vertical  </span> </p> </td> 
   <td colname="col2"> <p>Alineación de etiqueta vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Anchura de la etiqueta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para definir la etiqueta de tamaño de incrustación para que se alinee en la parte superior y tenga 80 píxeles de ancho:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

El ancho del cuadro combinado de tamaño incrustado se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7combobox
```

**Propiedades CSS del cuadro combinado**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Anchura del cuadro combinado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El cuadro combinado es compatible con el selector de atributos `expanded` con posibles valores `true` y `false`. `true` se utiliza cuando el cuadro combinado muestra uno de los tamaños de incrustación predefinidos, por lo que debe tener toda la anchura disponible. `false` se utiliza cuando se selecciona la opción de tamaño personalizado en el cuadro combinado, por lo que debe reducirse para permitir espacio para los campos de entrada de anchura y altura personalizados.

Ejemplo: para establecer el cuadro combinado del tamaño de incrustación en 300 píxeles de ancho al mostrar un elemento predefinido y 110 píxeles de ancho al mostrar un tamaño personalizado:

```
.s7ecatalogviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

La altura del texto del cuadro combinado se define mediante un elemento interno especial y se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**Propiedades CSS del texto del cuadro combinado**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del texto del cuadro combinado. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para establecer la altura del texto del cuadro combinado de tamaño incrustado en 40 píxeles:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

El cuadro combinado tiene un botón &quot;desplegable&quot; a la derecha y se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**Propiedades CSS del botón de cuadro combinado**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Posición del botón vertical dentro del cuadro combinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p>Posición del botón horizontal dentro del cuadro combinado. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p>Imagen de botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

Ejemplo: para establecer un botón desplegable en 28 x 28 píxeles y tener una imagen separada para cada estado:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

El panel con la lista de tamaños incrustados que se muestra al abrir el cuadro combinado se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7comboboxdropdown
```

El tamaño y la posición del panel están controlados por el componente. No es posible cambiarlo mediante CSS.

**Propiedades CSS de la lista desplegable de cuadro combinado**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde del panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para establecer que el panel del cuadro combinado tenga un borde gris de un píxel:

```
.s7ecatalogviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Un solo elemento de un panel desplegable que se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dropdownitemanchor
```

**Propiedades CSS del anclaje del elemento desplegable**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Fondo del elemento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para establecer que el elemento del panel del cuadro combinado tenga un fondo blanco:

```
.s7ecatalogviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Marca de verificación que se muestra a la izquierda del elemento seleccionado dentro del panel de cuadro combinado y que se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7checkmark
```

**Propiedades CSS de la casilla de verificación**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
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
   <td colname="col2"> <p>Imagen del elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para establecer el icono de marca de verificación en 25 x 25 píxeles:

```
.s7ecatalogviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Cuando se selecciona la opción &quot;Tamaño personalizado&quot; en el cuadro combinado Tamaño incrustado, el cuadro de diálogo muestra dos campos de entrada adicionales a la derecha para permitir al usuario introducir un tamaño incrustado personalizado. Estos campos se envuelven en un contenedor que se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsizepanel
```

**Propiedades CSS del panel de tamaño personalizado del cuadro de diálogo**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> izquierda </span> </p> </td> 
   <td colname="col2"> <p> Distancia desde el cuadro combinado de tamaño incrustado. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para establecer que el panel de campos de entrada de tamaño personalizado sea de 20 píxeles a la derecha del cuadro combinado:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Cada campo de entrada de tamaño personalizado se envuelve en un contenedor que procesa un borde y define el margen entre los campos. Se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsize
```

**Propiedades CSS del cuadro de diálogo de tamaño personalizado**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde alrededor del campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Ancho del campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen  </span> </p> </td> 
   <td colname="col2"> <p> Margen del campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Relleno de campo de entrada. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para definir los campos de entrada de tamaño personalizado con un borde gris de un píxel, margen, relleno y anchura de 70 píxeles:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Si se necesita desplazamiento vertical, la barra de desplazamiento se representa en el panel situado cerca del borde derecho del cuadro de diálogo, que se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogscrollpanel
```

**Propiedades CSS del panel de desplazamiento del cuadro de diálogo**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del panel de desplazamiento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un panel de desplazamiento con una anchura de 44 píxeles

```
.s7ecatalogviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

El aspecto del área de la barra de desplazamiento se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar
```

**Propiedades CSS de la barra de desplazamiento**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho de la barra de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento vertical de la barra de desplazamiento desde la parte superior del panel de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento vertical de la barra de desplazamiento desde la parte inferior del panel de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento horizontal de la barra de desplazamiento desde el borde derecho del panel de desplazamiento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una barra de desplazamiento de 28 píxeles de ancho y con un margen de ocho píxeles desde la parte superior, derecha e inferior del panel de desplazamiento:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

La barra de desplazamiento es el área entre los botones de desplazamiento superior e inferior. El componente establece automáticamente la posición y la altura de la pista. El seguimiento se controla con el siguiente selector de clase CSS

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**Propiedades CSS de la barra de desplazamiento**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Rastrear anchura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Rastrear color de fondo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una pista de barra de desplazamiento de 28 píxeles de ancho y con un fondo gris:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

La barra de desplazamiento se mueve verticalmente dentro de un área de seguimiento de desplazamiento. Su posición vertical está totalmente controlada por la lógica del componente. Sin embargo, la altura de la miniatura no cambia dinámicamente según la cantidad de contenido. La altura de la miniatura y otros aspectos se pueden configurar con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**Propiedades CSS de la barra de desplazamiento**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Anchura de la extremidad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura de la extremidad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno superior  </span> </p> </td> 
   <td colname="col2"> <p>El margen vertical entre la parte superior de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno inferior  </span> </p> </td> 
   <td colname="col2"> <p> El margen vertical entre la parte inferior de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p> La imagen mostrada para un estado de pulgar determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb es compatible con el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a diferentes estados de los pulgares: `up`, `down`, `over` y `disabled`.

Ejemplo: para configurar un control de barra de desplazamiento de 28 x 45 píxeles, tiene un margen de diez píxeles en la parte superior e inferior y tiene distintas ilustraciones para cada estado:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

El aspecto de los botones de desplazamiento superior e inferior se controla con los siguientes selectores de clase CSS:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

No es posible colocar botones de desplazamiento utilizando las propiedades CSS `top`, `left`, `bottom` y `right`. En su lugar, la lógica del visor los coloca automáticamente.

**Propiedades CSS de los botones de desplazamiento superior e inferior**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p> La imagen mostrada para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Estos botones admiten el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones: `up`, `down`, `over` y `disabled`.

La información sobre herramientas de botones se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: para configurar botones de desplazamiento de 28 x 32 píxeles y que tengan distintas ilustraciones para cada estado:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

