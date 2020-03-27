---
description: La barra de control secundaria es el área rectangular que contiene los botones Primera y Última página y un indicador de página cuando está disponible en CSS.
seo-description: La barra de control secundaria es el área rectangular que contiene los botones Primera y Última página y un indicador de página cuando está disponible en CSS.
seo-title: Barra de control secundaria
solution: Experience Manager
title: Barra de control secundaria
topic: Dynamic media
uuid: 9a91da6b-0d9b-4b4c-9659-86a64e624947
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Barra de control secundaria{#secondary-control-bar}

La barra de control secundaria es el área rectangular que contiene los botones Primera y Última página y un indicador de página cuando está disponible en CSS.

De forma predeterminada, solo se muestra en teléfonos móviles y se encuentra en la parte inferior del visor. Siempre se necesita toda la anchura del visor disponible. Es posible cambiar su color, altura y posición vertical mediante CSS, en relación con el contenedor del visor.

El aspecto de la barra de control secundaria se controla con el siguiente selector de clase CSS:

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la parte superior del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la parte inferior del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de la barra de control principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo de la barra de control secundaria. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una barra de control secundaria gris de 72 píxeles de altura y situada en la parte inferior del contenedor del visor.

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

