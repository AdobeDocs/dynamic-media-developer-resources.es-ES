---
title: Vista de zoom
description: La vista principal consiste en la imagen ampliable.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Vista de zoom{#zoom-view}

La vista principal consiste en la imagen ampliable.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área de visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7zoomviewer .s7zoomview
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
   <td colname="col2"> <p> Color de fondo en formato hexadecimal de la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Cursor mostrado sobre la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Hacer transparente la vista principal.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

En sistemas de escritorio, el componente admite `cursortype` selector de atributos que se puede aplicar a la clase `.s7zoomview`. Controla el tipo de cursor en función del estado del componente y la acción del usuario. Se admiten los siguientes `cursortype` valores:

* `default`

  Se muestra cuando la imagen no se puede ampliar debido a una resolución de imagen pequeña, a la configuración de componentes o a ambas cosas.

* `zoomin`

  Se muestra cuando se puede ampliar la imagen.

* `reset`

  Se muestra cuando la imagen está en el nivel de zoom máximo y se puede restablecer a su estado inicial.

* `drag`

  Se muestra cuando el usuario desplaza la imagen cuyo estado se ha ampliado.

* `slide`

  Se muestra cuando el usuario realiza un intercambio de imágenes mediante un deslizamiento o barrido horizontal.
