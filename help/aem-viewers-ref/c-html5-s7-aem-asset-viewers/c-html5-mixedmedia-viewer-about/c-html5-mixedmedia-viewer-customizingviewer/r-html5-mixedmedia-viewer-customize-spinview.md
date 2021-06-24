---
description: La vista principal consiste en la imagen de giro cuando el recurso actual es un conjunto de giros.
solution: Experience Manager
title: Vista de giro
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Developer,Business Practitioner
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# Vista de giro{#spin-view}

La vista principal consiste en la imagen de giro cuando el recurso actual es un conjunto de giros.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

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

Ejemplo: para que la vista de giro sea transparente.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
