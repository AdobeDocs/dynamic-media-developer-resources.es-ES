---
description: La vista principal consiste en la imagen ampliable.
seo-description: La vista principal consiste en la imagen ampliable.
seo-title: vista de zoom
solution: Experience Manager
title: vista de zoom
topic: Dynamic media
uuid: 34cb6c80-77eb-42b0-91dd-ae0369ea2881
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom view{#zoom-view}

La vista principal consiste en la imagen ampliable.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7zoomviewer .s7zoomview
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
   <td colname="col2"> <p>Se muestra el cursor sobre la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para que la vista principal sea transparente.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

En sistemas de escritorio, el componente admite el selector de `cursortype` atributos que se puede aplicar a la `.s7zoomview` clase. Controla el tipo de cursor según el estado del componente y la acción del usuario. The following `cursortype` values are supported:

* `default`

   Se muestra cuando la imagen no se puede ampliar debido a una pequeña resolución de imagen, a una configuración de componente o a ambos.

* `zoomin`

   Se muestra cuando se puede ampliar la imagen.

* `reset`

   Se muestra cuando la imagen está en el nivel máximo de zoom y se puede restablecer a su estado inicial.

* `drag`

   Se muestra cuando el usuario recorre la imagen que está en estado de zoom.

* `slide`

   Se muestra cuando el usuario realiza el intercambio de imágenes realizando un barrido horizontal o un gesto de gesto.

