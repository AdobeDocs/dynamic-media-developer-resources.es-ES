---
title: Área del visor principal
description: La zona de las vistas principales es la zona ocupada por las vistas principales y las muestras. Se configura para que se ajuste a la pantalla de dispositivo disponible cuando no se especifica ningún tamaño.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fe8b748c-5318-4fcd-9f3a-d50523bb3f8f
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# Área del visor principal{#main-viewer-area}

La zona de las vistas principales es la zona ocupada por las vistas principales y las muestras. Se configura para que se ajuste a la pantalla de dispositivo disponible cuando no se especifica ningún tamaño.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer 
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
.s7mixedmediaviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
