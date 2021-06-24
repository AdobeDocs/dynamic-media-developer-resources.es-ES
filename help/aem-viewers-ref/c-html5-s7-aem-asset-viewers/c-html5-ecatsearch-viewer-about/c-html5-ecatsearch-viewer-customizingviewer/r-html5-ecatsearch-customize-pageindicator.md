---
description: El indicador de página muestra el índice de página actual y el recuento total de páginas. Aparece en la barra de control principal en sistemas de escritorio y tabletas, en teléfonos móviles se agrega a la barra de control secundaria. CSS puede cambiar el tamaño, el aspecto y la posición del indicador de página.
solution: Experience Manager
title: Indicador de página
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Developer,Business Practitioner
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 4%

---

# Indicador de página{#page-indicator}

El indicador de página muestra el índice de página actual y el recuento total de páginas. Aparece en la barra de control principal en sistemas de escritorio y tabletas, en teléfonos móviles se agrega a la barra de control secundaria. CSS puede cambiar el tamaño, el aspecto y la posición del indicador de página.

El indicador de página de aspecto visual se controla con el siguiente selector de clase CSS:

`.s7ecatalogsearchviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Sitúe la palanca desde el borde superior de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p>Sitúe la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles) desde el borde derecho, incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> izquierda </span> </p> </td> 
   <td colname="col2"> <p>Sitúe el borde izquierdo de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Sitúe el borde inferior de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nombre de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un indicador de página de 56 x 28 píxeles, centrado horizontalmente y colocado 4 píxeles desde la parte inferior de la barra de control principal, y utilizar una fuente Helvetica de 14 píxeles.

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
