---
title: Imprimir
description: La herramienta Imprimir consiste en un botón añadido a la barra de control y el cuadro de diálogo modal que se muestra cuando se activa la herramienta.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c5939cdc-fa4e-4f19-b2a9-21b389492c4f
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 2%

---

# Imprimir{#print}

La herramienta Imprimir consiste en un botón añadido a la barra de control y el cuadro de diálogo modal que se muestra cuando se activa la herramienta.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del botón de impresión se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7print
```

**Propiedades CSS del botón de impresión**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento desde la parte superior de la barra de control. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> La distancia al botón siguiente de la izquierda o del lado izquierdo de la barra de control si este botón es el primero de una fila. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite la variable `state` selector de atributos, que se puede utilizar para aplicar diferentes aspectos a distintos estados de botones.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: para configurar un botón de impresión de 28 x 28 píxeles y muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes.

```
.s7ecatalogsearchviewer .s7print { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7print[state='up'] { 
background-image:url(images/v2/Print_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7print[state='over'] { 
background-image:url(images/v2/Print_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7print[state='down'] { 
background-image:url(images/v2/Print_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7print[state='disabled'] { 
background-image:url(images/v2/Print_dark_disabled.png); 
}
```

La superposición de fondo que cubre la página web cuando el cuadro de diálogo está activo, se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
```

**Propiedades CSS de la superposición**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidad </span> </p> </td> 
   <td colname="col2"> <p> Opacidad de la superposición de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de superposición de fondo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar la superposición de fondo para que sea gris con un 70 % de opacidad:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

De forma predeterminada, el cuadro de diálogo modal se muestra centrado en la pantalla de los sistemas de escritorio. El componente gestiona el posicionamiento y el tamaño del cuadro de diálogo. El cuadro de diálogo se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**Propiedades CSS del cuadro de diálogo**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Radio del borde del cuadro de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo del cuadro de diálogo; </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para configurar un cuadro de diálogo para que tenga un fondo gris:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

El encabezado del cuadro de diálogo consta de un icono, un texto de título y un botón de cierre. El contenedor de encabezado se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
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

El icono y el texto del título se envuelven en un contenedor adicional controlado con lo siguiente:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
```

**CSS properties of the dialog line**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Margen interior para el icono y el título del encabezado. </p> </td> 
  </tr> 
 </tbody> 
</table>

Header icon is controlled with the following CSS class selector:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
```

**Propiedades CSS del icono de encabezado del cuadro de diálogo**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Icon image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

El título del encabezado se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
```

**CSS properties of the dialog box header text**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Altura de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
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
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen interior del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen de botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite la variable `state` selector de atributos, que se puede utilizar para aplicar diferentes aspectos a distintos estados de botones.

La información del objeto del botón Cerrar y el título del cuadro de diálogo se pueden localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: para configurar el encabezado del cuadro de diálogo con relleno, icono de 22 x 22 píxeles y título en negrita de 16 puntos. Finalmente, un botón Cerrar de 28 x 28 píxeles colocó dos píxeles desde la parte superior y dos píxeles desde la parte derecha del contenedor de cuadro de diálogo:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgprint_cap.png"); 
    height: 22px; 
    width: 22px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

El pie de página del cuadro de diálogo consta de los botones Cancelar y Enviar a impresión. El contenedor de pie de página se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
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

El pie de página tiene un contenedor interior que mantiene ambos botones. Se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
```

**Propiedades CSS del contenedor de botones de cuadro de diálogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Margen interior entre el pie de página y los botones. </p> </td> 
  </tr> 
 </tbody> 
</table>

El botón Cancelar se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
```

**Propiedades CSS del botón Cancelar del cuadro de diálogo**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Color del texto del botón para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Button background color for each state. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite la variable `state` selector de atributos, que se puede utilizar para aplicar diferentes aspectos a distintos estados de botones.

El botón Enviar a impresión se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**CSS properties of the dialog box action button**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Button width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Button height. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Button text color for each state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Button background color for each state. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which can be used to apply different skins to different button states.

Además, ambos botones comparten una clase CSS común que puede contener ajustes CSS que son los mismos para otros botones del cuadro de diálogo:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
```

**Propiedades CSS del botón**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de la fuente del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Altura del texto dentro del botón. Afecta a la alineación vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-Shadow </span> </p> </td> 
   <td colname="col2"> <p>Sombra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>Margen del botón derecho. </p> </td> 
  </tr> 
 </tbody> 
</table>

La información sobre herramientas de botones se puede localizar. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) for more information.

Example - To set up a dialog box footer with 64 x 34 Cancel button and a 96 x 34 Send to Print button, with the text color and background color different for each button state:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton { 
 width:96px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

El área de diálogo principal (entre el encabezado y el pie de página) contiene contenido de cuadro de diálogo. En todos los casos, el componente administra la anchura de esta área, no es posible configurarla en CSS. El área de diálogo principal se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**Propiedades CSS del área de visualización del cuadro de diálogo **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altura del área principal del cuadro de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del área del cuadro de diálogo principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Margen exterior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un área de diálogo principal para que tenga una altura calculada automáticamente, tenga un margen de diez píxeles y utilice un fondo blanco:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

Todo el contenido del formulario (como etiquetas y campos de entrada) reside dentro de un contenedor controlado con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
```

**Propiedades CSS del cuerpo del cuadro de diálogo **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Configurar el contenido del formulario para que tenga un relleno de diez píxeles:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

El formulario del cuadro de diálogo se rellena línea a línea, donde cada línea tiene una parte del contenido del formulario (como una etiqueta y un campo de entrada de texto). Single form line is controlled with the following CSS class selector:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**CSS properties of the dialog box line**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen de línea interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - To set up a dialog box form to have ten pixel padding for each line:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

El tamaño del bloque de contenido del cuadro de diálogo se controla con el siguiente selector de clase CSS:

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**Propiedades CSS del ancho de entrada del cuadro de diálogo**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho del bloque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Margen de línea interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para definir un bloque de contenido con una anchura de 430 píxeles y con un relleno de 10 píxeles en la parte inferior:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Todas las etiquetas estáticas del formulario del cuadro de diálogo se controlan con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
```

Esta clase no es adecuada para controlar el tamaño o la posición de la etiqueta porque puede aplicarla a textos en varios lugares de la interfaz de usuario del formulario.

**CSS properties of the dialog box label. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Grosor de fuente de la etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente de la etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Label font family. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color del texto de la etiqueta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Las etiquetas de los cuadros de diálogo se pueden localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Example - to set up all labels to be gray, bold, with a nine pixel font:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Input controls are wrapped into the container and controlled with the following CSS class selector:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**Propiedades CSS del contenedor de entrada del cuadro de diálogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left </span> </p> </td> 
   <td colname="col2"> <p>Margen interior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para establecer un relleno de 30 píxeles desde el borde izquierdo del cuadro de diálogo.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

Los botones de opción y el texto de su rótulo se controlan con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**Propiedades CSS de la opción de cuadro de diálogo**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho total del botón de radio con un rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color del texto del rótulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El espaciado entre el botón de radio y su rótulo se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**Propiedades CSS de la entrada de opciones del cuadro de diálogo**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p> Espaciado entre el botón de radio y su rótulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Los selectores numéricos para la selección del rango de impresión se controlan con el siguiente selector de clase CSS

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**CSS properties of the dialog box print range**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Anchura del selector numérico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen </span> </p> </td> 
   <td colname="col2"> <p> Espaciado alrededor del selector numérico. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar todos los botones de radio para que tengan una anchura de 150 píxeles con texto negro, un espaciado de diez píxeles y un selector numérico de 42 píxeles de ancho:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption { 
    color: #000000; 
    width: 150px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption input { 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange { 
    margin-left: 10px; 
    margin-right: 10px; 
    width: 42px; 
}
```

El divisor horizontal entre la selección del rango de páginas y las secciones de diseño de impresión se controla con el siguiente selector de clase CSS:

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**Propiedades CSS del divisor horizontal**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p> Border around divider. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Inner padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del divisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen </span> </p> </td> 
   <td colname="col2"> <p>Margen exterior </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a 430 pixel-wide grey divider with a 10 pixel vertical padding on both sides, and a ten pixel margin at the top:

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```
