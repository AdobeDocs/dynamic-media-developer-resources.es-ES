---
title: Definir indicador
description: Establecer indicador es una serie de puntos que se representan sobre las muestras cuando se utiliza un visor en un dispositivo táctil. Los puntos ayudan a los usuarios a navegar por las páginas de miniaturas cuando los botones de desplazamiento no están disponibles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---

# Definir indicador{#set-indicator}

Establecer indicador es una serie de puntos que se representan sobre las muestras cuando se utiliza un visor en un dispositivo táctil. Los puntos ayudan a los usuarios a navegar por las páginas de miniaturas cuando los botones de desplazamiento no están disponibles.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del indicador determinado**

El aspecto del contenedor del indicador determinado se controla con el siguiente selector de clase CSS:

```
.s7zoomviewer .s7setindicator
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>El color de fondo en formato hexadecimal del indicador determinado. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para crear un indicador de conjunto con un fondo blanco:

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

El aspecto de un punto indicador de conjunto individual se controla con el selector de clases CSS:

`.s7zoomviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del punto del indicador definido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del punto del indicador definido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>Margen izquierdo en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>Margen superior en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>Margen derecho en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>Margen inferior en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Radio de borde en píxeles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo en formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El punto del indicador definido admite `state` selector de atributos, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de miniaturas. En particular, `state="selected"` corresponde a la página actual de miniaturas, `state="unselected"` corresponde al estado de punto predeterminado.

Ejemplo: Para crear un punto de indicador definido de 15 x 15 píxeles, con un margen horizontal de 2 píxeles, un margen superior de 5 píxeles, un margen inferior de 1 píxel, un radio de 12 píxeles, #D5D3D3 color predeterminado y #939393 color activo:

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
