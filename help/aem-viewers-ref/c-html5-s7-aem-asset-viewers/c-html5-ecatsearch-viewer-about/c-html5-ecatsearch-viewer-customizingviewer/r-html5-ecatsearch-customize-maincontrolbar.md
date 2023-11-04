---
title: Barra de control principal
description: La barra de control principal es el área rectangular de los sistemas de escritorio y tabletas que contiene todos los controles de la interfaz de usuario (excepto los botones de página grande) disponibles para el visor de búsqueda en el catálogo electrónico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cee6a4d4-4099-4bc8-9d67-00a1e963a139
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 1%

---

# Barra de control principal{#main-control-bar}

La barra de control principal es el área rectangular de los sistemas de escritorio y tabletas que contiene todos los controles de la interfaz de usuario (excepto los botones de página grande) disponibles para el visor de búsqueda en el catálogo electrónico.

En los teléfonos móviles, sigue conservando los botones Miniaturas, Tabla de contenido, Descargar, Imprimir, Favoritos, Compartir en redes sociales, Pantalla completa y Cerrar. Sin embargo, los botones Primera página y Última página y el Indicador de página se quitan de la barra de control principal y se agregan a la barra de control secundaria en su lugar. De forma predeterminada, la barra de control principal se muestra en la parte superior del área del visor en sistemas de escritorio y teléfonos móviles, y se mueve a la parte inferior del área del visor en tabletas. Siempre ocupa toda la anchura del visor disponible. Es posible cambiar el color, la altura y la posición vertical en CSS en relación con el contenedor del visor.

El aspecto de la barra de control principal se controla con el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la parte superior del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la parte inferior del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de la barra de control principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo de la barra de control principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo** : para configurar una barra de control principal gris de 36 píxeles de altura y situada en la parte superior del contenedor del visor.

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

La barra de control principal admite una función de desplazamiento opcional. Se activa si la anchura del visor es demasiado pequeña y no hay espacio suficiente para ajustar todos los botones preestablecidos en la barra de control. En este caso, aparece un botón de flecha de dos estados en el lado derecho de la barra de control. Al tocar o hacer clic en este botón, se desplazan todos los elementos de la barra de control a la izquierda o a la derecha, en función del estado del botón de desplazamiento. El caso de uso principal de esta función son los dispositivos móviles con pantallas pequeñas en orientación vertical.

La función de desplazamiento está activada para la barra de control principal y desactivada para la barra de control secundaria. La función se activa y desactiva mediante el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición </span> </p> </td> 
   <td colname="col2"> <p>Cuando se establece en <span class="codeph"> estático </span> la función de desplazamiento está desactivada. </p> <p>Establezca esta propiedad como <span class="codeph"> absoluto </span> para activar la función de desplazamiento. </p> </td> 
  </tr> 
 </tbody> 
</table>

El botón de desplazamiento se agrega a un elemento contenedor especial que coloca el botón correctamente. Permite aplicar un estilo diferente al área que rodea al botón y al resto del fondo de la barra de control en caso de que el alto del botón de desplazamiento sea menor que el alto de la barra de control.

El aspecto de este contenedor de botones de desplazamiento se controla con el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Normalmente debe ser igual o mayor que la anchura del botón de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del contenedor. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puede cambiar el tamaño y la apariencia del botón de desplazamiento mediante CSS.

El aspecto de este botón se controla con el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el `state` y `selected` selectores de atributos, que se pueden utilizar para aplicar diferentes aspectos a diferentes estados de botones. En particular, `state="selected"` corresponde al estado inicial del botón de desplazamiento cuando es posible desplazar el contenido de la barra de control hacia la izquierda. El `state="default"` corresponde al estado en el que el contenido se desplaza completamente hacia la izquierda y el botón de desplazamiento sugiere devolverlo al estado inicial.

La información del objeto del botón se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

**Ejemplo** - Para activar la función de desplazamiento en la barra de control principal para teléfonos móviles. Y configure un botón de desplazamiento de 64 x 64 píxeles que muestre una imagen diferente para cada uno de los 4 estados de botón diferentes cuando se selecciona o no se selecciona:

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```
