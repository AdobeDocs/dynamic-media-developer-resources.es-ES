---
title: Información sobre herramientas
description: En los sistemas de escritorio, algunos elementos de la interfaz de usuario, como los botones, tienen información sobre herramientas que se muestra al pasar el ratón por encima.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 706b27a1-99e8-4596-8bd1-af4455501e29
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 6%

---

# Información sobre herramientas{#tooltips}

En los sistemas de escritorio, algunos elementos de la interfaz de usuario, como los botones, tienen información sobre herramientas que se muestra al pasar el ratón por encima.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto de las informaciones de objeto se controla con el siguiente selector de clase CSS:

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Radio del borde de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde-color </span> </p> </td> 
   <td colname="col2"> <p> Color del borde del fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color de texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nombre de fuente del texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente del texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>En caso de que los estilos de información sobre herramientas se personalicen desde la página web de incrustación, todas las propiedades deben contener `!IMPORTANT` regla. Esta regla no es necesaria si la información de objeto se personaliza en el archivo CSS del visor.

Ejemplo: para configurar informaciones de objeto que tengan un borde gris con un radio de esquina de tres píxeles, un fondo negro y un texto blanco escrito con Arial®, un tamaño de 11 píxeles:

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
