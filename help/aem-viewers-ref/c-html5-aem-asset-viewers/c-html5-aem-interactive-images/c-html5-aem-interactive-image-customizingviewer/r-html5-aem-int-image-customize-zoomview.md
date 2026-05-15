---
title: Vista de zoom
description: La vista principal consiste en la imagen estática.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: e83d53a1-bee9-4e4d-8295-a3a350f3ff9c
TQID: 'https://experienceleague.adobe.com/udgNJ6m1EffqVOmFwnWqMYoRDP22isq2zKvgDK4KNLo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 1%

---

# Vista de zoom{#zoom-view}

La vista principal consiste en la imagen estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área de visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7interactiveimage .s7zoomview
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
 </tbody> 
</table>

Ejemplo: para hacer transparente la vista principal.

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```
