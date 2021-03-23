---
description: En los sistemas de escritorio, algunos elementos de la interfaz de usuario, como los botones, tienen información sobre herramientas que se muestra al pasar el ratón por encima.
seo-description: En los sistemas de escritorio, algunos elementos de la interfaz de usuario, como los botones, tienen información sobre herramientas que se muestra al pasar el ratón por encima.
seo-title: Información sobre herramientas
solution: Experience Manager
title: Información sobre herramientas
uuid: 4cf5ce32-136e-4612-b550-715d51cef982
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---


# Información del objeto{#tooltips}

En los sistemas de escritorio, algunos elementos de la interfaz de usuario, como los botones, tienen información sobre herramientas que se muestra al pasar el ratón por encima.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto de la información del objeto se controla con el siguiente selector de clases CSS:

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
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Radio del borde de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde-color  </span> </p> </td> 
   <td colname="col2"> <p> Color del borde del fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color de texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nombre de fuente del texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente del texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Si los estilos de información del objeto se personalizan desde la página web de incrustación, todas las propiedades deben contener la regla `!IMPORTANT`. Esto no es necesario si la información del objeto se personaliza en el archivo CSS del visor.

Ejemplo: para configurar información del objeto con un borde gris con un radio de esquina de 3 píxeles, fondo negro y texto blanco en Arial, con un tamaño de 11 píxeles:

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

