---
description: La vista principal consiste en la imagen del catálogo. Se puede realizar un barrido para llegar a otra página o ampliar.
solution: Experience Manager
title: Vista de la página
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Developer,Business Practitioner
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 4%

---

# Vista de la página{#page-view}

La vista principal consiste en la imagen del catálogo. Se puede realizar un barrido para llegar a otra página o ampliar.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7pageview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo de la vista principal en formato hexadecimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>Cursor que se muestra sobre la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para que la vista principal sea transparente.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

En los sistemas de escritorio, el componente admite el selector de atributos `cursortype` que se puede aplicar a la clase `.s7pageview` y controla el tipo del cursor en función del estado del componente y la acción del usuario. Se admiten los siguientes `cursortype` valores:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> predeterminado </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando la imagen no se puede ampliar debido a una pequeña resolución de imagen, a la configuración de componentes o a ambos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina  </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando se puede ampliar la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> restablecer </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando la imagen se encuentra en el nivel de zoom máximo y se puede restablecer al estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastrar </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando el usuario panorámica la imagen que está en estado de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva  </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando el usuario realiza un intercambio de imágenes realizando un barrido horizontal o una flexión. </p> </td> 
  </tr> 
 </tbody> 
</table>

El divisor de páginas que separa visualmente las páginas izquierda y derecha de la extensión del catálogo se controla con el siguiente selector de clases CSS:

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho del divisor de páginas. Configúrelo en <span class="codeph"> 0 </span> px para ocultar completamente el divisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p>La imagen que desea usar como divisor de página. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para tener un divisor de página de 40 píxeles de ancho con una imagen semitransparente.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Cuando el modificador `frametransition` se establece en `turn` o `auto` (en sistemas de escritorio), el aspecto del divisor de páginas se controla con el modificador `pageturnstyle` y se ignora la clase CSS `.s7pagedivider`.

Es posible configurar la visualización de los cursores personalizados del ratón sobre el área del visor principal. Esto se controla con los selectores de atributos adicionales aplicados a la clase CSS `.s7ecatalogsearchviewer .s7pageview`:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> predeterminado </span> </p> </td> 
   <td colname="col2"> <p> Normalmente es una flecha que se muestra para la imagen no ampliable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina  </span> </p> </td> 
   <td colname="col2"> <p> Muestra cuándo se puede ampliar una imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> restablecer </span> </p> </td> 
   <td colname="col2"> <p>Muestra cuándo una imagen tiene el máximo zoom y se puede restablecer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastrar </span> </p> </td> 
   <td colname="col2"> <p>Muestra cuándo el usuario realiza la operación de arrastrar en la imagen ampliada </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva  </span> </p> </td> 
   <td colname="col2"> <p>Muestra cuándo el usuario realiza el intercambio de imágenes mediante el gesto de diapositiva </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: tener diferentes cursores del ratón para cada tipo de estado del componente.

```
.s7ecatalogsearchviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
