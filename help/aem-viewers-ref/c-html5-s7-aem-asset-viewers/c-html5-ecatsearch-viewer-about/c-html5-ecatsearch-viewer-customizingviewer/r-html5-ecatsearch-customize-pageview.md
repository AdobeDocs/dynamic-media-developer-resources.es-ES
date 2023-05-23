---
title: Vista de la página
description: La vista principal consiste en la imagen del catálogo. Se puede deslizar para llegar a otra página o ampliar.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 4%

---

# Vista de la página{#page-view}

La vista principal consiste en la imagen del catálogo. Se puede deslizar para llegar a otra página o ampliar.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo de la vista principal en formato hexadecimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Cursor que se muestra sobre la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para hacer transparente la vista principal.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

En sistemas de escritorio, el componente admite el `cursortype` selector de atributos que se puede aplicar a `.s7pageview` y controla el tipo de cursor en función del estado del componente y la acción del usuario. Lo siguiente `cursortype` se admiten estos valores:

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
   <td colname="col2"> <p>Se muestra cuando la imagen no se puede ampliar debido a una resolución de imagen pequeña, a la configuración del componente o a ambas cosas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoom </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando se puede ampliar la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> restablecer </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando la imagen está en el nivel de zoom máximo y se puede restablecer al estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastrar </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando el usuario desplaza la imagen cuyo estado se ha ampliado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando el usuario realiza un intercambio de imágenes realizando un barrido o un gesto horizontal. </p> </td> 
  </tr> 
 </tbody> 
</table>

El divisor de páginas que separa visualmente las páginas izquierda y derecha del pliego de catálogos se controla con el siguiente selector de clases CSS:

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho del divisor de página. Configure como. <span class="codeph"> 0 </span> px para ocultar el divisor por completo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>La imagen que desea utilizar como divisor de página. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Tener un divisor de página de 40 píxeles de ancho con imagen semitransparente.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Si la variable `frametransition` El modificador se ha definido en `turn` o `auto` (en sistemas de escritorio), el aspecto del divisor de página se controla con la variable `pageturnstyle` y el modificador `.s7pagedivider` Se omite la clase CSS.

Es posible configurar la visualización de los cursores personalizados del ratón sobre el área principal del visor. Esta capacidad se controla con los selectores de atributos adicionales aplicados a `.s7ecatalogsearchviewer .s7pageview` Clase CSS:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> predeterminado </span> </p> </td> 
   <td colname="col2"> <p> Normalmente, una flecha muestra la imagen no ampliable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoom </span> </p> </td> 
   <td colname="col2"> <p> Muestra cuándo se puede ampliar una imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> restablecer </span> </p> </td> 
   <td colname="col2"> <p>Muestra cuándo una imagen está en el zoom máximo y se puede restablecer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastrar </span> </p> </td> 
   <td colname="col2"> <p>Muestra cuándo el usuario realiza una operación de arrastre en una imagen ampliada </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva </span> </p> </td> 
   <td colname="col2"> <p>Muestra cuándo el usuario realiza un intercambio de imágenes mediante el gesto de diapositiva </p> </td> 
  </tr> 
 </tbody> 
</table>

Por ejemplo: tenga diferentes cursores de ratón para cada tipo de estado de componente.

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
