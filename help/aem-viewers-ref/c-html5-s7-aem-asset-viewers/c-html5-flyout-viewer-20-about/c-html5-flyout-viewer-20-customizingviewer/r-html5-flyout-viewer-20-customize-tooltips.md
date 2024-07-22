---
title: Tooltips
description: En sistemas de escritorio, algunos elementos de la interfaz de usuario, como los botones, incluyen información sobre herramientas que se muestra al pasar el ratón por encima.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 57d26a76-f4ee-44d5-b7a5-f3eb5c2a8759
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Tooltips{#tooltips}

En sistemas de escritorio, algunos elementos de la interfaz de usuario, como los botones, incluyen información sobre herramientas que se muestra al pasar el ratón por encima.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área de visor principal**

El aspecto de la información del objeto se controla con el siguiente selector de clase CSS:

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> borde-radio </span> </p> </td> 
   <td colname="col2"> <p> Radio de borde de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de borde </span> </p> </td> 
   <td colname="col2"> <p> Color de borde de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color del texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nombre de fuente del texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente del texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>En caso de que los estilos de información del objeto se personalicen desde la página web en la que se incorpora, todas las propiedades deben contener la regla `!IMPORTANT`. Sin embargo, no es necesario si la información del objeto se personaliza en el archivo CSS del visor.

Ejemplo: para configurar información de objeto que tenga un borde gris con un radio de esquina de 3 píxeles, fondo negro y texto blanco escrito con Arial®, tamaño de 11 píxeles:

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
