---
description: La vista principal consiste en la imagen ampliable.
seo-description: La vista principal consiste en la imagen ampliable.
seo-title: Vista de zoom
solution: Experience Manager
title: Vista de zoom
uuid: 34cb6c80-77eb-42b0-91dd-ae0369ea2881
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# Vista de zoom{#zoom-view}

La vista principal consiste en la imagen ampliable.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo en formato hexadecimal de la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>El cursor se muestra sobre la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para que la vista principal sea transparente.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

En los sistemas de escritorio, el componente admite el selector de atributos `cursortype` que se puede aplicar a la clase `.s7zoomview`. Controla el tipo del cursor en función del estado del componente y la acción del usuario. Se admiten los siguientes `cursortype` valores:

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

