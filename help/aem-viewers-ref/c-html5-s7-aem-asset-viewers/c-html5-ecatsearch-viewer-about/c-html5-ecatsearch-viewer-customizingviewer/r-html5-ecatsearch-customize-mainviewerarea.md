---
description: El área de vista principal es el área ocupada por la imagen del catálogo. Normalmente se configura para que se ajuste a la pantalla de dispositivo disponible cuando no se especifica ningún tamaño.
solution: Experience Manager
title: Área del visor principal
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Developer,Business Practitioner
exl-id: 854f5fa7-f46d-4c4f-9a44-886fec93f606
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '124'
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo en formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar un visualizador con un fondo blanco ( `#FFFFFF`) y hacer que su tamaño sea de 512 x 288 píxeles.

```
.s7ecatalogsearchviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
