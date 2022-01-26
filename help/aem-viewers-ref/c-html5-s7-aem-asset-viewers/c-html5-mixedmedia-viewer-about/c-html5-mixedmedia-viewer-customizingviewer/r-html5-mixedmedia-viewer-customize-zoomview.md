---
title: Vista de zoom
description: En el modo de zoom continuo, la vista principal consiste en la imagen ampliable cuando el recurso actual es una sola imagen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Vista de zoom{#zoom-view}

En el modo de zoom continuo, la vista principal consiste en la imagen ampliable cuando el recurso actual es una sola imagen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7zoomview
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

Ejemplo: para que la vista de zoom sea transparente.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

En sistemas de escritorio, el componente es compatible `cursortype` selector de atributos que se puede aplicar a la variable `.s7zoomview` Clase . Controla el tipo del cursor en función del estado del componente y la acción del usuario. Lo siguiente `cursortype` son compatibles:

* `default`

   Se muestra cuando la imagen no se puede ampliar debido a una pequeña resolución de imagen, a la configuración de componentes o a ambos.

* `zoomin`

   Se muestra cuando se puede ampliar la imagen.

* `reset`

   Se muestra cuando la imagen se encuentra en el nivel de zoom máximo y se puede restablecer a su estado inicial.

* `drag`

   Se muestra cuando el usuario panorámica la imagen que está en estado de zoom.

* `slide`

   Se muestra cuando el usuario realiza el intercambio de imágenes realizando un barrido horizontal o un gesto de gafa.
