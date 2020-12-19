---
description: La vista principal consiste en la imagen de giro cuando el recurso actual es un conjunto de giros.
seo-description: La vista principal consiste en la imagen de giro cuando el recurso actual es un conjunto de giros.
seo-title: Vista de giros
solution: Experience Manager
title: Vista de giros
topic: Dynamic media
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Vista de giro{#spin-view}

La vista principal consiste en la imagen de giro cuando el recurso actual es un conjunto de giros.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col2"> <p> Color de fondo en formato hexadecimal de la vista de giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para hacer transparente la vista de giro.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

