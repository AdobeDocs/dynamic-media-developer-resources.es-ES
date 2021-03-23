---
description: La zona de vista principal es la zona ocupada por las vistas flotantes y las muestras.
seo-description: La zona de vista principal es la zona ocupada por las vistas flotantes y las muestras.
seo-title: Área del visor principal
solution: Experience Manager
title: Área del visor principal
uuid: 828ee8e5-8e5f-47cf-a566-2e997a5e3926
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom en línea
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---


# Área del visor principal{#main-viewer-area}

La zona de vista principal es la zona ocupada por las vistas flotantes y las muestras.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7flyoutviewer
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

Ejemplo: para configurar un visor flotante con fondo blanco ( `#FFFFFF`) y lograr su tamaño de 260 x 500 píxeles.

```
.s7flyoutviewer { 
 background-color: #FFFFFF; 
 width: 260px; 
 height: 500px;  
}
```

