---
title: Indicador de página
description: El indicador de página muestra el índice de página actual y el recuento total de páginas. Aparece en la barra de control principal de los sistemas de escritorio y tabletas; en los teléfonos móviles se agrega a la barra de control secundaria. CSS puede cambiar el tamaño, aplicar un aspecto y colocar el indicador de página.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 4%

---

# Indicador de página{#page-indicator}

El indicador de página muestra el índice de página actual y el recuento total de páginas. Aparece en la barra de control principal de los sistemas de escritorio y tabletas; en los teléfonos móviles se agrega a la barra de control secundaria. CSS puede cambiar el tamaño, aplicar un aspecto y colocar el indicador de página.

El indicador de página de apariencia se controla con el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde superior de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde derecho de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> izquierda </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde izquierdo de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde inferior de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del indicador de página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del indicador de página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nombre de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un indicador de página de 56 x 28 píxeles, centrado horizontalmente y colocado a 4 píxeles de la parte inferior de la barra de control principal, y utilice una fuente Helvetica® de 14 píxeles.

```
.s7ecatalogsearchviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```
