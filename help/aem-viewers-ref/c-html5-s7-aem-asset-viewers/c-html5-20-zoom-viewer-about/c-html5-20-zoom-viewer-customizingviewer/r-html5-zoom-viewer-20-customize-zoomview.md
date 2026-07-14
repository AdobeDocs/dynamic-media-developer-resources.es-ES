---
title: Vista de zoom
description: La vista principal consiste en la imagen ampliable.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
TQID: 'https://experienceleague.adobe.com/i1B2r5g74xmk6H3DLD12gyRI9uJo32p3SmgS-OFnLf8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 171
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

