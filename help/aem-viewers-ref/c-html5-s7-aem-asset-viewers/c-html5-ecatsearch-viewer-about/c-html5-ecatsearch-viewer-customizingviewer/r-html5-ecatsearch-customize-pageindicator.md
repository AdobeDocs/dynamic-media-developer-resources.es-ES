---
title: Indicador de página
description: El indicador de página muestra el índice de página actual y el recuento total de páginas. Aparece en la barra de control principal de los sistemas de escritorio y tabletas; en los teléfonos móviles se agrega a la barra de control secundaria. CSS puede cambiar el tamaño, aplicar un aspecto y colocar el indicador de página.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
TQID: 'https://experienceleague.adobe.com/QikQn00CFMxmnTEXKZcTifhXC-SBmW-IC9VbKlZ7TGY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 0%

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
   <td colname="col1"> <p> <span class="codeph"> </span> principales </p> </td> 
   <td colname="col2"> <p>Posición desde el borde superior de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecho </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde derecho de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dejó </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde izquierdo de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde el borde inferior de la barra de control principal (en sistemas de escritorio y tabletas) o la barra de control secundaria (en teléfonos móviles), incluido el relleno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Anchura del indicador de página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
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
