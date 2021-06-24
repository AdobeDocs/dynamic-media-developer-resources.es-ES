---
description: El indicador de conjunto es una serie de puntos representados sobre muestras cuando se utiliza un visor en un dispositivo táctil. Los puntos ayudan a los usuarios a navegar por las páginas de miniaturas cuando los botones de desplazamiento no están disponibles.
solution: Experience Manager
title: Definir indicador
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Developer,Business Practitioner
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# Definir indicador{#set-indicator}

El indicador de conjunto es una serie de puntos representados sobre muestras cuando se utiliza un visor en un dispositivo táctil. Los puntos ayudan a los usuarios a navegar por las páginas de miniaturas cuando los botones de desplazamiento no están disponibles.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del indicador de conjunto**

El aspecto del contenedor de indicador establecido se controla con el siguiente selector de clase CSS:

```
.s7zoomviewer .s7setindicator
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
   <td colname="col2"> <p>Color de fondo en formato hexadecimal del indicador establecido. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un indicador de conjunto con un fondo blanco:

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

El aspecto de un punto indicador de conjunto individual se controla con el selector de clase CSS:

`.s7zoomviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del punto indicador definido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del punto indicador definido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p>Margen izquierdo en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p>Margen superior en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right  </span> </p> </td> 
   <td colname="col2"> <p>Margen derecho en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom  </span> </p> </td> 
   <td colname="col2"> <p>Margen inferior en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Radio del borde en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo en formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El punto indicador definido es compatible con el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a diferentes estados de miniaturas. En concreto, `state="selected"` corresponde a la página actual de miniaturas, `state="unselected"` corresponde al estado de punto predeterminado.

Ejemplo: para configurar el punto indicador definido para que sea de 15 x 15 píxeles, con dos píxeles de margen horizontal, cinco píxeles de margen superior, un píxel de margen inferior, doce píxeles de radio, #D5D3D3 de color predeterminado y #939393 de color activo:

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
