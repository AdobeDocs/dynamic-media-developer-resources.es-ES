---
title: Correo electrónico compartido
description: La herramienta de uso compartido de correo electrónico consiste en un botón agregado al panel de uso compartido de Social y el cuadro de diálogo modal que se muestra cuando se activa la herramienta. La posición del botón se administra completamente mediante la herramienta Compartir en redes sociales.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1788e069-68dd-4960-bc49-34ffdf29991a
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '3023'
ht-degree: 0%

---

# Correo electrónico compartido{#email-share}

La herramienta de uso compartido de correo electrónico consiste en un botón agregado al panel de uso compartido de Social y el cuadro de diálogo modal que se muestra cuando se activa la herramienta. La posición del botón se administra completamente mediante la herramienta Compartir en redes sociales.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del botón de uso compartido de correo electrónico se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emailshare
```

**Propiedades CSS de la herramienta de uso compartido de correo electrónico**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

Es posible quitar el botón del panel Compartir en redes sociales estableciendo la propiedad CSS `display:none` en su clase CSS.

La información del objeto del botón se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar un botón de uso compartido de correo electrónico de 28 x 28 píxeles y que muestre una imagen diferente para cada uno de los cuatro estados de botón diferentes.

```
.s7videoviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7videoviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7videoviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7videoviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

La superposición de fondo que cubre la página web cuando el cuadro de diálogo está activo, se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7backoverlay
```

**Propiedades CSS de la superposición posterior**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidad </span> </p> </td> 
   <td colname="col2"> <p> Opacidad de superposición de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de superposición de fondo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar la superposición de fondo para que sea gris con una opacidad del 70 %:

```
.s7videoviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

De forma predeterminada, el cuadro de diálogo modal se muestra centrado en la pantalla de los sistemas de escritorio y ocupa toda el área de la página web en los dispositivos táctiles. En todos los casos, el componente gestiona la colocación y el tamaño del cuadro de diálogo. El cuadro de diálogo se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialog
```

**Propiedades CSS del cuadro de diálogo**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde-radio </span> </p> </td> 
   <td colname="col2"> <p> Radio del borde del cuadro de diálogo (en caso de que el cuadro de diálogo no ocupe toda la ventana del explorador); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo del cuadro de diálogo; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> Debe estar desconfigurado o configurado al 100%, en cuyo caso el cuadro de diálogo ocupa toda la ventana del explorador (este modo es preferido en dispositivos táctiles); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> Debe estar desconfigurado o configurado al 100 %, en cuyo caso el cuadro de diálogo ocupa toda la ventana del explorador (este modo se prefiere en dispositivos táctiles). </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar el cuadro de diálogo para que utilice toda la ventana del explorador y tenga un fondo blanco en los dispositivos táctiles:

```
.s7videoviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

El encabezado del cuadro de diálogo consta de un icono, un texto de título y un botón de cierre. El contenedor de encabezado se controla con el siguiente selector de clase CSS

```
.s7videoviewer .s7emaildialog .s7dialogheader
```

**Propiedades CSS del encabezado del cuadro de diálogo**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Relleno interno del contenido del encabezado. </p> </td> 
  </tr> 
 </tbody> 
</table>

El icono y el texto del título se envuelven en un contenedor adicional controlado con

```
.s7videoviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**Propiedades CSS de la línea de diálogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Relleno interior para el icono y el título del encabezado </p> </td> 
  </tr> 
 </tbody> 
</table>

El icono de encabezado se controla con el siguiente selector de clase CSS

```
.s7videoviewer .s7emaildialog .s7dialogheadericon
```

**Propiedades CSS del icono de encabezado del cuadro de diálogo**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

El título del encabezado se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogheadertext
```

**Propiedades CSS del texto del encabezado del cuadro de diálogo**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Altura de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno de texto interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

El botón Cerrar se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7closebutton
```

**Propiedades CSS del ** de botón Cerrar

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> principales </p> </td> 
   <td colname="col2"> <p> Posición vertical del botón en relación con el contenedor de encabezado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecho </span> </p> </td> 
   <td colname="col2"> <p> Posición horizontal del botón relativa al contenedor del encabezado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen de botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

Se puede localizar la información del objeto del botón Cerrar y el título del cuadro de diálogo. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: Para configurar el encabezado del cuadro de diálogo con relleno, icono de 24 x 17 píxeles, título de 16 puntos en negrita y botón de cierre de 28 x 28 píxeles. Y finalmente, colóquelo a dos píxeles de la parte superior y a dos píxeles de la derecha del contenedor de diálogo:

```
.s7videoviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

El pie de página del cuadro de diálogo consta de los botones &quot;cancelar&quot; y &quot;enviar correo electrónico&quot;. El contenedor de pie de página se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogfooter
```

**Propiedades CSS de la ** de pie de página del cuadro de diálogo

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p> Borde que se puede utilizar para separar visualmente el pie de página del resto del cuadro de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El pie de página tiene un contenedor interno que mantiene ambos botones. Se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogbuttoncontainer
```

**Propiedades CSS del contenedor de botones del cuadro de diálogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Relleno interior entre el pie de página y los botones. </p> </td> 
  </tr> 
 </tbody> 
</table>

El botón Cancelar se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogcancelbutton
```

**Propiedades CSS del botón Cancelar del cuadro de diálogo**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Color del texto del botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo del botón para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

El botón Enviar correo electrónico se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogactionbutton
```

**Propiedades CSS del botón de acción del cuadro de diálogo**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Color del texto del botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo del botón para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

Además, ambos botones comparten una clase CSS común que puede contener configuraciones de CSS iguales para otros botones de cuadro de diálogo:

```
.s7videoviewer .s7emaildialog .s7dialogfooter .s7button
```

**Propiedades CSS del botón**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes Button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura de línea </span> </p> </td> 
   <td colname="col2"> <p> Altura del texto dentro del botón. Afecta a la alineación vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>Sombra paralela. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen derecho </span> </p> </td> 
   <td colname="col2"> <p>Margen del botón derecho. </p> </td> 
  </tr> 
 </tbody> 
</table>

La información sobre herramientas de los botones se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar un pie de página de cuadro de diálogo con un botón Cancelar de 64 x 34 y un botón Enviar correo electrónico de 82 x 34, con el color del texto y el color de fondo diferentes para cada estado de botón:

```
.s7videoviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

El área de diálogo principal, entre el encabezado y el pie de página, contiene contenido de cuadro de diálogo desplazable y panel de desplazamiento a la derecha. En todos los casos, el componente administra la anchura de esta área, no es posible establecerla en CSS. El área del cuadro de diálogo principal se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogviewarea
```

**Propiedades CSS de la ** del área de visualización del cuadro de diálogo

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> Alto del área del cuadro de diálogo principal. Sólo debe especificarse cuando el cuadro de diálogo funciona en modo escritorio. No es aplicable cuando el tamaño del cuadro de diálogo es tal que ocupa toda la ventana del explorador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del área del cuadro de diálogo principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen </span> </p> </td> 
   <td colname="col2"> <p>Margen exterior. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El área del cuadro de diálogo principal admite el selector de atributos `state` opcional. Se establece en `sendsuccess` cuando se envía el formulario de correo electrónico y el cuadro de diálogo muestra un mensaje de confirmación. Siempre que el mensaje de confirmación sea pequeño, se puede utilizar este selector de atributos para reducir la altura del cuadro de diálogo cuando se muestre dicho mensaje de confirmación.

Ejemplo: Para configurar el área del cuadro de diálogo principal para que tenga inicialmente una altura de 300 píxeles y una altura de 100 píxeles cuando se muestre el mensaje de confirmación, tenga un margen de diez píxeles y utilice un fondo blanco:

```
.s7videoviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7videoviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

Todo el contenido del formulario (como etiquetas y campos de entrada) reside dentro de un contenedor controlado con

```
.s7videoviewer .s7emaildialog .s7dialogbody
```

Si la altura de este contenedor parece ser mayor que el área del cuadro de diálogo principal, el componente activa automáticamente un desplazamiento vertical.

**Propiedades CSS del ** de cuerpo del cuadro de diálogo

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar el contenido del formulario para que tenga un relleno de diez píxeles:

```
.s7videoviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

El formulario de cuadro de diálogo se rellena línea a línea, donde cada línea lleva una parte del contenido del formulario (como una etiqueta y un campo de entrada de texto). Una sola línea de formulario se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**Propiedades CSS de la línea del cuadro de diálogo**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno de línea interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un formulario de cuadro de diálogo con un relleno de diez píxeles para cada línea:

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

Todas las etiquetas estáticas del formulario de cuadro de diálogo se controlan con

```
.s7videoviewer .s7emaildialog .s7dialoglabel
```

Esta clase no es adecuada para controlar el tamaño o la posición de las etiquetas porque puede aplicarla a textos en varios lugares de la interfaz de usuario del formulario.

**Propiedades CSS de la etiqueta del cuadro de diálogo. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente de etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente de etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes de etiquetas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color de texto de etiqueta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Las etiquetas del cuadro de diálogo se pueden localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar todas las etiquetas como grises, negrita con una fuente de nueve píxeles:

```
.s7videoviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Todas las etiquetas estáticas que se muestran a la izquierda de los campos de entrada del formulario se controlan con:

```
.s7videoviewer .s7emaildialog .s7dialoginputlabel
```

**Propiedades CSS de la etiqueta de entrada del cuadro de diálogo**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho de la etiqueta estática. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alineación de texto </span> </p> </td> 
   <td colname="col2"> <p>Alineación horizontal del texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen </span> </p> </td> 
   <td colname="col2"> <p>Margen de etiqueta estático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno de etiqueta estático. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar las etiquetas de los campos de entrada para que tengan una anchura de 50 píxeles, alineadas a la derecha, tengan diez píxeles de relleno y un margen de diez píxeles a la derecha:

```
.s7videoviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Cada campo de entrada de formulario está ajustado en el contenedor, que permite aplicar un borde personalizado alrededor del campo de entrada. Se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialoginputcontainer
```

**Propiedades CSS del contenedor de entrada del cuadro de diálogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde alrededor del contenedor de campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El contenedor de campos de entrada admite el selector de atributos `state` opcional. Se establece en `verifyerror` cuando el usuario comete un error en el formato de datos de entrada y la validación en línea falla. Este selector de atributos se puede utilizar para resaltar entradas de usuario incorrectas en el formulario.

La mayoría de los campos de entrada que se extienden desde la etiqueta de la izquierda hasta el borde derecho del cuerpo del cuadro de diálogo (que incluye el campo &quot;desde&quot; y el campo &quot;mensaje&quot;) se controlan con:

```
.s7videoviewer .s7emaildialog .s7dialoginputwide
```

**Propiedades CSS del campo que abarca toda la entrada del cuadro de diálogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del campo de entrada. </p> </td> 
  </tr> 
 </tbody> 
</table>

El campo de entrada &quot;Para&quot; es más estrecho porque asigna espacio para el botón &quot;eliminar correo electrónico&quot; de la derecha. Se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialoginputshort
```

**Propiedades CSS del campo corto de entrada del cuadro de diálogo**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del campo de entrada. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configurar un formulario para que tenga un borde gris de un píxel con nueve píxeles de relleno alrededor de todos los campos de entrada. Para tener el mismo borde en color rojo para los campos que no superan la validación, debe tener 250 píxeles de ancho en el campo de entrada &quot;Hasta&quot; y el resto de los campos de entrada 300 píxeles de ancho:

```
.s7videoviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

El campo de entrada de mensaje de correo electrónico también se controla con:

```
.s7videoviewer .s7emaildialog .s7dialogmessage
```

Esta clase le permite establecer propiedades específicas para el elemento `TEXTAREA` subyacente.

**Propiedades CSS del mensaje del cuadro de diálogo**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ajuste de palabras </span> </p> </td> 
   <td colname="col2"> <p>Estilo de ajuste de palabras. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un mensaje de correo electrónico de 50 píxeles de alto y usar el ajuste de palabras `break-word`:

```
.s7videoviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

El botón &quot;Añadir otra dirección de correo electrónico&quot; permite al usuario agregar más de una dirección en el formulario de correo electrónico. Se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton
```

**Propiedades CSS del botón Agregar dirección de correo electrónico del cuadro de diálogo**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color del texto del botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen de botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p>Posición de la imagen del botón dentro del área de botones. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes Button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura de línea </span> </p> </td> 
   <td colname="col2"> <p>Altura del texto dentro del botón. Afecta a la alineación vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alineación de texto </span> </p> </td> 
   <td colname="col2"> <p>Alineación de texto horizontal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

La información del objeto del botón se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar el botón &quot;Añadir otra dirección de correo electrónico&quot; para que tenga 25 píxeles de altura, utilice una fuente en negrita de 12 puntos con alineación derecha y un color de texto e imagen diferentes para cada estado:

```
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

El botón &quot;Eliminar&quot; permite al usuario eliminar direcciones adicionales del formulario de correo electrónico. Se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton
```

**Las propiedades CSS del cuadro de diálogo quitan el botón de correo electrónico**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen de botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

La información del objeto del botón se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar un botón &quot;Eliminar&quot; de 25 x 25 píxeles y utilizar una imagen diferente para cada estado:

```
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

El contenido que se comparte se muestra en la parte inferior del cuerpo del cuadro de diálogo e incluye una miniatura, un título, la dirección URL de origen y una descripción. Se envuelve en un recipiente controlado con:

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**Propiedades CSS del ** de contenido del cuadro de diálogo

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde del contenedor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un contenedor inferior para que tenga un borde punteado de un píxel sin relleno:

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

La imagen en miniatura se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogthumbnail
```

La propiedad `background-image` está establecida por la lógica del componente.

**Propiedades CSS de la imagen en miniatura del cuadro de diálogo**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Anchura de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura de miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alinear verticalmente </span> </p> </td> 
   <td colname="col2"> <p>Miniatura de alineación vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar la miniatura para que sea de 90 x 60 píxeles y alineada en la parte superior con diez píxeles de relleno:

```
.s7videoviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

El título, el origen y la descripción del contenido se agrupan además en un panel a la derecha de la miniatura de contenido. Se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialoginfopanel
```

**Propiedades CSS del panel de información del cuadro de diálogo**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un panel de información de contenido con un ancho de 300 píxeles:

```
.s7videoviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

El título de contenido se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogtitle
```

**Propiedades CSS del título del cuadro de diálogo**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen </span> </p> </td> 
   <td colname="col2"> <p>Margen exterior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un título de contenido para que utilice una fuente en negrita y tenga un margen de diez píxeles:

```
.s7videoviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

El origen del contenido se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogorigin
```

**Propiedades CSS del ** de origen de contenido del cuadro de diálogo

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen </span> </p> </td> 
   <td colname="col2"> <p>Margen exterior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar el origen del contenido para que tenga un margen de diez píxeles:

```
.s7videoviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

La descripción del contenido se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogdescription
```

**Propiedades CSS de la descripción del contenido del cuadro de diálogo**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen </span> </p> </td> 
   <td colname="col2"> <p>Margen exterior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una descripción de contenido para que tenga un margen de diez píxeles y utilice una fuente de nueve puntos:

```
.s7videoviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

Cuando un usuario introduce datos de entrada incorrectos y falla la validación en línea, o cuando el cuadro de diálogo debe representar un error o un mensaje de confirmación cuando se envía el formulario, se muestra un mensaje en la parte superior del cuerpo del cuadro de diálogo. Se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogerrormessage
```

**Mensaje de error en las propiedades CSS del cuadro de diálogo**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p> Icono de error. El valor predeterminado es un signo de exclamación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Posición del icono de error dentro del área de mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color del texto del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura de línea </span> </p> </td> 
   <td colname="col2"> <p> Altura del texto dentro del mensaje. Afecta a la alineación vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este mensaje admite el selector de atributos `state` con los siguientes valores posibles: `verifyerror`, `senderror` y `sendsuccess`. El selector de atributos `verifyerror` se establece cuando se muestra un mensaje debido a un error de validación de entrada en línea; `senderror` se establece cuando un servicio de correo electrónico back-end informa de un error; `sendsuccess` se establece cuando el correo electrónico se envía correctamente. De este modo, es posible aplicar un estilo diferente al mensaje en función del estado del cuadro de diálogo.

El mensaje de error se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: Para configurar un mensaje para que utilice una fuente en negrita de diez puntos. Además, debe tener una altura de línea de 25 píxeles, un relleno de 20 píxeles a la izquierda, usar un icono de signo de exclamación, texto rojo si hay un error, y ningún icono y texto verde si hay éxito:

```
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

Si se necesita desplazamiento vertical, la barra de desplazamiento se procesa en el panel cerca del borde derecho del cuadro de diálogo, que se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7dialogscrollpanel
```

**Propiedades CSS del panel de desplazamiento del cuadro de diálogo**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del panel de desplazamiento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un panel de desplazamiento con un ancho de 44 píxeles:

```
.s7videoviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

El aspecto del área de la barra de desplazamiento se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7scrollbar
```

**Propiedades CSS de la barra de desplazamiento**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> Ancho de la barra de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> principales </p> </td> 
   <td colname="col2"> <p> Desplazamiento de la barra de desplazamiento vertical desde la parte superior del panel de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento vertical de la barra desde la parte inferior del panel de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecho </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento de la barra de desplazamiento horizontal desde el borde derecho del panel de desplazamiento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una barra de desplazamiento que tenga 28 píxeles de ancho, un margen de ocho píxeles desde la parte superior, derecha e inferior del panel de desplazamiento:

```
.s7videoviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

La pista de la barra de desplazamiento es el área entre los botones de desplazamiento superior e inferior. El componente establece automáticamente la posición y la altura de la pista. El seguimiento se controla con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**Propiedades CSS de la pista de desplazamiento**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>El ancho de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>El color de fondo de la pista. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una pista de barra de desplazamiento que tenga 28 píxeles de ancho y un fondo gris:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

El pulgar de la barra de desplazamiento se mueve verticalmente dentro de un área de pista de desplazamiento. Su posición vertical está totalmente controlada por la lógica del componente, pero la altura de la miniatura no cambia dinámicamente según la cantidad de contenido. Puede configurar la altura de la miniatura y otros aspectos con el siguiente selector de clase CSS:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**Propiedades CSS de la miniatura de la barra de desplazamiento**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>La anchura del pulgar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>La altura del pulgar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno superior </span> </p> </td> 
   <td colname="col2"> <p> El margen vertical entre la parte superior de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno inferior </span> </p> </td> 
   <td colname="col2"> <p> El margen vertical entre la parte inferior de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de miniatura determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura admite el selector de atributos `state`, que se puede utilizar para aplicar distintas apariencias a diferentes estados de la miniatura: `up`, `down`, `over` y `disabled`.

La información sobre herramientas de los botones se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obtener más información.

Ejemplo: para configurar el miniatura de la barra de desplazamiento de 28 x 45 píxeles, tiene un margen de diez píxeles en la parte superior e inferior y tiene diferentes ilustraciones para cada estado:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

El aspecto de los botones de desplazamiento superior e inferior se controla con los siguientes selectores de clase CSS:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton  
  
```

**Propiedades CSS de los botones de desplazamiento superior e inferior**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>La altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Estos botones admiten el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones: `up`, `down`, `over` y `disabled`.

Ejemplo: para configurar botones de desplazamiento de 28 x 32 píxeles con ilustraciones diferentes para cada estado:

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
