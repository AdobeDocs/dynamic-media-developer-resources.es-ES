---
title: Barra de control secundaria
description: La barra de control secundaria es el área rectangular que contiene los botones Primera y Última página y un indicador de página cuando están disponibles en CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 2354c3a0-2df7-4a18-aac1-fac158a9b659
TQID: 'https://experienceleague.adobe.com/aT-NQikSvfT9khT6idoN9HcN6oDJBzJv6zoo0G8wg1g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 0%

---

# Barra de control secundaria{#secondary-control-bar}

La barra de control secundaria es el área rectangular que contiene los botones Primera y Última página y un indicador de página cuando están disponibles en CSS.

De forma predeterminada, solo se muestra en teléfonos móviles y se coloca en la parte inferior del visor. Siempre toma todo el ancho de visor disponible. CSS permite cambiar el color, la altura y la posición vertical en relación con el contenedor del visor.

El aspecto de la barra de control secundaria se controla con el siguiente selector de clase CSS:

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> principales </p> </td> 
   <td colname="col2"> <p>Posición desde la parte superior del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior </span> </p> </td> 
   <td colname="col2"> <p>Posición desde la parte inferior del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura de la barra de control principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
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
