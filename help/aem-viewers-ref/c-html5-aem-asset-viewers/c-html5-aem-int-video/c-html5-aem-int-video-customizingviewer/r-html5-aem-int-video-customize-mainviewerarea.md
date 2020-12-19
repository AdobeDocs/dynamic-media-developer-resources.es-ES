---
description: El área de vista principal es el área ocupada por las muestras interactivas. Normalmente se configura para que se ajuste a la pantalla del dispositivo disponible cuando no se especifica ningún tamaño.
seo-description: El área de vista principal es el área ocupada por las muestras interactivas. Normalmente se configura para que se ajuste a la pantalla del dispositivo disponible cuando no se especifica ningún tamaño.
seo-title: Área del visor principal
solution: Experience Manager
title: Área del visor principal
topic: Dynamic media
uuid: 3e04c578-dcb2-4034-8809-dc949be80097
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---


# Área del visor principal{#main-viewer-area}

El área de vista principal es el área ocupada por las muestras interactivas. Normalmente se configura para que se ajuste a la pantalla del dispositivo disponible cuando no se especifica ningún tamaño.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7interactivevideoviewer
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

## Ejemplo {#section-ee18025b182a42dc98052de5f133ddfe}

Para configurar un visor con un fondo blanco ( `#FFFFFF`) y hacer que su tamaño sea de 512 x 288 píxeles.

```
.s7interactivevideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

