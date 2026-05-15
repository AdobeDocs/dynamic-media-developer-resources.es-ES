---
title: Vista de giro
description: La vista principal consiste en la imagen de giro cuando el recurso actual es un conjunto de giros.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
TQID: 'https://experienceleague.adobe.com/i51Si1u-npMCR4Rum5-g3JRjShCBWXG54yam4BWpU84'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 1%

---

# Vista de giro{#spin-view}

La vista principal consiste en la imagen de giro cuando el recurso actual es un conjunto de giros.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área de visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col2"> <p> Color de fondo en formato hexadecimal de la vista de giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para hacer transparente la vista de giro.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
