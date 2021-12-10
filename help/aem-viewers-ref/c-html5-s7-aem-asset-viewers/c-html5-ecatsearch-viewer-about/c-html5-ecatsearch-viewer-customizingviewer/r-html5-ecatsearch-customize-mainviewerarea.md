---
title: Área del visor principal
description: El área de vista principal es el área ocupada por la imagen del catálogo. Normalmente se configura para que se ajuste a la pantalla de dispositivo disponible cuando no se especifica ningún tamaño.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 854f5fa7-f46d-4c4f-9a44-886fec93f606
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# Área del visor principal{#main-viewer-area}

El área de vista principal es el área ocupada por la imagen del catálogo. Normalmente se configura para que se ajuste a la pantalla de dispositivo disponible cuando no se especifica ningún tamaño.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo en formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Configuración de un visor con un fondo blanco ( `#FFFFFF`) y hacer su tamaño 512 x 288 píxeles.

```
.s7ecatalogsearchviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
