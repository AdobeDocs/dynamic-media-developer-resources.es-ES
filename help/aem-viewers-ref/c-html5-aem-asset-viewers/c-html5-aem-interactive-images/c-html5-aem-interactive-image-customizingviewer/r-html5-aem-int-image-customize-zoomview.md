---
description: La vista principal consiste en la imagen estática.
seo-description: La vista principal consiste en la imagen estática.
seo-title: Vista de zoom
solution: Experience Manager
title: Vista de zoom
topic: Dynamic Media
uuid: d8349f8c-134f-4e74-9d0c-ab56981965d7
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---


# Vista de zoom{#zoom-view}

La vista principal consiste en la imagen estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7interactiveimage .s7zoomview
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
 </tbody> 
</table>

Ejemplo: para que la vista principal sea transparente.

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```

