---
title: Vista de zoom
description: La vista principal consiste en la imagen ampliable.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 286b9df4-88db-4e5d-aab4-9cbe01195e57
TQID: 'https://experienceleague.adobe.com/ub5sNABbFHA-V5yaiNmUAHZ1NwTGIlzNecIL5KlJPg4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 165
ht-degree: 1%

---

# Vista de zoom{#zoom-view}

La vista principal consiste en la imagen ampliable.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área de visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col2"> <p>El cursor se muestra sobre la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para hacer transparente la vista principal.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

En sistemas de escritorio, el componente admite el selector de atributos `cursortype` que se puede aplicar a la clase `.s7zoomview` y controla el tipo de cursor en función del estado del componente y la acción del usuario. Se admiten los siguientes `cursortype` valores:

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
   <td colname="col2"> <p>Se muestra cuando la imagen no se puede ampliar debido a una resolución de imagen pequeña, a la configuración de componentes o a ambas cosas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoom </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando se puede ampliar la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> restableció </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando la imagen está en el nivel de zoom máximo y se puede restablecer a su estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastrar </span> </p> </td> 
   <td colname="col2"> <p>Se muestra cuando un usuario explora la imagen que está en estado de ampliación. </p> </td> 
  </tr> 
 </tbody> 
</table>
