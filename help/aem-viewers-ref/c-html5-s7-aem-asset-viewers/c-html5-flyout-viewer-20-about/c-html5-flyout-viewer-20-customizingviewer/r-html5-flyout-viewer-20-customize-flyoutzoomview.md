---
title: Vista de zoom flotante
description: La vista principal consta de la imagen estática y la imagen ampliada que se muestra en la vista flotante. También consta del área de navegación de resalte que se muestra sobre la imagen estática y el mensaje de sugerencia que se muestra sobre la imagen estática.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Vista de zoom flotante{#flyout-zoom-view}

La vista principal consta de la imagen estática y la imagen ampliada que se muestra en la vista flotante. También consta del área de navegación de resalte que se muestra sobre la imagen estática y el mensaje de sugerencia que se muestra sobre la imagen estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si las dimensiones de la imagen que se está visualizando no coinciden con las dimensiones de la vista de zoom flotante, el contenido de la imagen se centra dentro del área de visualización rectangular de la vista de zoom flotante.

**Propiedades CSS de la vista principal**

El aspecto de la vista principal se controla con el siguiente selector de clase CSS:

```
.s7flyoutviewer .s7flyoutzoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo de la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para hacer transparente la vista principal:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Propiedades CSS de la vista flotante**

El aspecto de la vista flotante se controla con el siguiente selector de clase CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dejó </span> </p> </td> 
   <td colname="col2"> <p> La posición horizontal de la vista flotante, en relación con la esquina superior izquierda de la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> principales </p> </td> 
   <td colname="col2"> <p> Posición vertical de la vista flotante, con relación a la esquina superior izquierda de la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> Ancho de la vista flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura de la vista flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde de la vista flotante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una vista flotante en 600 x 400 píxeles, que aparece con un desplazamiento de 100 píxeles a la derecha de la vista principal de 512 x 288 que se muestra en el ejemplo anterior:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**Propiedades CSS del resaltado en la vista principal**

El aspecto del resaltado en la vista principal se controla con el siguiente selector de clase CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

Es posible controlar los atributos de fondo, borde, transparencia y similares mediante CSS. Sin embargo, el tamaño y la posición del elemento DOM de resaltado se administran mediante la lógica del visor. No se admite la anulación mediante CSS.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p> El color del resaltado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidad </span> </p> </td> 
   <td colname="col2"> <p> Resaltar la opacidad. </p> <p>Para Internet Explorer 8, utilice el filtro <span class="codeph">: alpha(opacity-...) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>El resaltado de borde. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar el resaltado verde con un 40 % de transparencia y un borde rojo de un píxel:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Propiedades CSS del cursor**

Cuando el parámetro `highlightmode` está establecido en `cursor`, el área resaltada en la vista principal se reemplaza con ilustraciones de cursor de tamaño fijo, que se controla con el selector de clase CSS:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

Es posible controlar la imagen de fondo y el tamaño mediante CSS.

Las propiedades CSS aplicables incluyen:

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Ilustración del cursor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del cursor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del cursor. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El cursor admite el selector de atributos `input`, que se puede utilizar para aplicar ilustraciones de cursor y tamaños diferentes para distintos dispositivos. En particular, `input="mouse"` corresponde a los sistemas de escritorio y `input="touch"` a los dispositivos táctiles.

**Propiedades CSS de la superposición**

Cuando el parámetro `overlay` se establece en `1`, el área alrededor del marco de resaltado o la imagen del cursor se controla con el selector de clases CSS:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de superposición. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidad </span> </p> </td> 
   <td colname="col2"> <p>Opacidad de superposición. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Propiedades CSS del mensaje de sugerencia**

El aspecto del mensaje de sugerencia se controla con el siguiente selector de clase CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

Es posible configurar el estilo, el tamaño, el aspecto y el desplazamiento vertical de la fuente mediante CSS. Sin embargo, la alineación horizontal la administra la lógica del visor. No se admite anularlo mediante CSS utilizando las propiedades `left` o `right`.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior </span> </p> </td> 
   <td colname="col2"> <p>Desplazamiento desde la parte inferior de la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color del texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nombre de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno alrededor del texto del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de relleno de fondo del texto del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde-radio </span> </p> </td> 
   <td colname="col2"> <p>Radio del borde de fondo del texto del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidad </span> </p> </td> 
   <td colname="col2"> <p>Opacidad de fondo del texto del mensaje. </p> <p>Para Internet Explorer 8, use <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

El mensaje de sugerencia se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) para obtener más información.

Ejemplo: para configurar un mensaje de sugerencia semitransparente con una fuente Arial® blanca de 12 píxeles, un desplazamiento de 50 píxeles desde la parte inferior de la vista principal, relleno y borde redondeado:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
