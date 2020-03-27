---
description: La vista principal consiste en la imagen ampliable.
seo-description: La vista principal consiste en la imagen ampliable.
seo-title: vista de zoom
solution: Experience Manager
title: vista de zoom
topic: Dynamic media
uuid: 06464e36-8c9c-4d3c-b4e5-5911f002568c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom view{#zoom-view}

La vista principal consiste en la imagen ampliable.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo en formato hexadecimal de la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>El cursor se muestra sobre la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para que la vista principal sea transparente.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

En sistemas de escritorio, el componente admite el selector de `cursortype` atributos que se puede aplicar a la `.s7zoomview` clase y controla el tipo de cursor en función del estado del componente y la acción del usuario. The following `cursortype` values are supported:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> predeterminado </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando la imagen no se puede ampliar debido a una pequeña resolución de imagen, a una configuración de componente o a ambos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando se puede ampliar la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> restablecer </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando la imagen está en el nivel máximo de zoom y se puede restablecer a su estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastrar </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando un usuario gira la imagen que está en estado de zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

