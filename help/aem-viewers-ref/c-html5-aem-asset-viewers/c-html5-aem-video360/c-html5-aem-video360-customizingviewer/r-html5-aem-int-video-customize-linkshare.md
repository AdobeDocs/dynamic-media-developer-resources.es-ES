---
title: Vínculos compartidos
description: La herramienta para compartir vínculos consiste en un botón agregado al panel Compartir en redes sociales y el cuadro de diálogo modal que se muestra cuando se activa la herramienta. La posición del botón se administra completamente mediante la herramienta Compartir en redes sociales.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 9eb2ef38-9b86-4c60-90a2-6609cb3fcc39
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# Vínculos compartidos{#link-share}

La herramienta para compartir vínculos consiste en un botón agregado al panel Compartir en redes sociales y el cuadro de diálogo modal que se muestra cuando se activa la herramienta. La posición del botón se administra completamente mediante la herramienta Compartir en redes sociales.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

El aspecto del botón para compartir vínculos se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkshare
```

**Propiedades CSS de la herramienta para compartir vínculos**

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
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

Es posible quitar el botón del panel Compartir en redes sociales estableciendo la propiedad CSS `display:none` en su clase CSS.

La información del objeto del botón se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Ejemplo: para configurar un botón de uso compartido de vínculos de 28 x 28 píxeles y mostrar una imagen diferente para cada uno de los cuatro estados de botón diferentes:

```
.s7video360viewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7video360viewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7video360viewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7video360viewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

La superposición de fondo que cubre la página web cuando el cuadro de diálogo está activo, se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7backoverlay
```

**Propiedades CSS de la superposición en segundo plano**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidad </span> </p> </td> 
   <td colname="col2"> <p>Opacidad de superposición de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de superposición de fondo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** - para configurar una superposición de fondo para que sea gris con una opacidad del 70%:

```
.s7video360viewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

De forma predeterminada, el cuadro de diálogo modal se muestra centrado en la pantalla de los sistemas de escritorio y ocupa toda el área de la página web en los dispositivos táctiles. En todos los casos, el componente gestiona la colocación y el tamaño del cuadro de diálogo. El cuadro de diálogo se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialog
```

**Propiedades CSS del cuadro de diálogo**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde-radio </span> </p> </td> 
   <td colname="col2"> <p> Radio del borde del cuadro de diálogo, en caso de que el cuadro de diálogo no ocupe todo el explorador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del cuadro de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Debe estar desconfigurado o configurado al 100 %, en cuyo caso el cuadro de diálogo ocupa toda la ventana del explorador (este modo es preferido en dispositivos táctiles). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Debe estar desconfigurado o configurado al 100 %, en cuyo caso el cuadro de diálogo ocupa toda la ventana del explorador (este modo es preferido en dispositivos táctiles). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** - para configurar el cuadro de diálogo para que utilice toda la ventana del explorador y tenga un fondo blanco en los dispositivos táctiles:

```
.s7video360viewer.s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

El encabezado del cuadro de diálogo consta de un icono, un texto de título y un botón de cierre. El contenedor de encabezado se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialogheader
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

El icono y el texto del título se envuelven en un contenedor adicional controlado con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline
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
.s7video360viewer .s7linkdialog .s7dialogheadericon
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
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

El título del encabezado se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialogheadertext
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
.s7video360viewer .s7linkdialog .s7closebutton
```

**Propiedades CSS del &#x200B;** de botón Cerrar

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
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

Se puede localizar la información del objeto del botón Cerrar y el título del cuadro de diálogo. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Ejemplo** - Para configurar un encabezado de cuadro de diálogo con relleno, icono de 22 x 12 píxeles y un título en negrita de 16 puntos. Y, por último, un botón Cerrar de 28 x 28 píxeles situado a dos píxeles de la parte superior y a dos píxeles de la derecha del contenedor del cuadro de diálogo:

```
.s7video360viewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

El pie de página del cuadro de diálogo consta de un botón Cancelar. El contenedor de pie de página se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialogfooter
```

**Propiedades CSS de la &#x200B;** de pie de página del cuadro de diálogo

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p> Borde que se puede utilizar para separar visualmente el pie de página del resto del cuadro de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El pie de página tiene un contenedor interno que mantiene el botón. Se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer
```

**Propiedades CSS del contenedor de botones del cuadro de diálogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Relleno interno entre el pie de página y el botón. </p> </td> 
  </tr> 
 </tbody> 
</table>

El botón Seleccionar todo se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialogactionbutton
```

El botón sólo está disponible en sistemas de escritorio.

**Propiedades CSS del botón Seleccionar todo**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
>El botón Seleccionar todo es compatible con el selector de atributos `state`, que se puede utilizar para aplicar distintas máscaras a distintos estados de botón.

El botón Cancel se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialogcancelbutton
```

**Propiedades CSS del cuadro de diálogo Botón Cancelar**

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

Además, ambos botones comparten una clase CSS común que puede contener configuraciones de CSS iguales para otros botones de cuadro de diálogo:

```
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button
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

La información sobre herramientas de los botones se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Ejemplo** - para configurar un pie de página de cuadro de diálogo con un botón Cancelar de 64 x 34, con colores de fondo y color de texto diferentes para cada estado de botón:

```
.s7video360viewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

El área de diálogo principal, entre el encabezado y el pie de página, contiene contenido de diálogo. En todos los casos, el componente administra la anchura de esta área; no es posible establecerla en CSS. El área del cuadro de diálogo principal se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialogviewarea
```

**Propiedades CSS de la &#x200B;** del área de visualización del cuadro de diálogo

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

**Ejemplo** - para configurar un área de cuadro de diálogo principal con una altura de 300 píxeles, tener un margen de 10 píxeles y usar un fondo blanco:

```
.s7video360viewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Todo el contenido del formulario, como las etiquetas y los campos de entrada, reside dentro de un contenedor controlado con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialogbody
```

**Propiedades CSS del &#x200B;** de cuerpo del cuadro de diálogo

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** - para configurar el contenido del formulario para que tenga un relleno de diez píxeles:

```
.s7interactivevideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

Todas las etiquetas estáticas del formulario de cuadro de diálogo se controlan con

```
.s7video360viewer .s7linkdialog .s7dialoglabel
```

Esta clase no es adecuada para controlar el tamaño o la posición de la etiqueta porque puede aplicarla a textos en varios lugares de la interfaz de usuario del formulario.

**Propiedades CSS de la etiqueta del cuadro de diálogo. &#x200B;**

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

Las etiquetas del cuadro de diálogo se pueden localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Ejemplo** - para configurar todas las etiquetas para que sean de color gris, utilice negrita con una fuente de nueve píxeles:

```
.s7video360viewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

El tamaño de la copia de texto que se muestra sobre el vínculo se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialoginputwide
```

**Propiedades CSS del campo que abarca toda la entrada del cuadro de diálogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** - para establecer que la copia de texto tenga un ancho de 430 píxeles y un relleno de 10 píxeles en la parte inferior:

```
.s7video360viewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

El vínculo compartido se envuelve en un contenedor y se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialoginputcontainer
```

**Propiedades CSS del contenedor de entrada del cuadro de diálogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde alrededor del contenedor de vínculo compartido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** - para establecer un borde gris de un píxel alrededor del texto del código incrustado y tener nueve píxeles de relleno:

```
.s7video360viewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

El vínculo compartido en sí se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7linkdialog .s7dialoglink
```

**Propiedades CSS del vínculo compartido del cuadro de diálogo**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Compartir la anchura del vínculo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** - para establecer que el vínculo compartido tenga un ancho de 450 píxeles:

```
.s7video360viewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```
