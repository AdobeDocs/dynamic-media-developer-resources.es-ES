---
description: El área de vista principal es la zona ocupada por el video 360. Normalmente se configura para que se ajuste a la pantalla del dispositivo disponible cuando no se especifica ningún tamaño.
seo-description: El área de vista principal es la zona ocupada por el video 360. Normalmente se configura para que se ajuste a la pantalla del dispositivo disponible cuando no se especifica ningún tamaño.
seo-title: Área del visor principal
solution: Experience Manager
title: Área del visor principal
topic: Dynamic media
uuid: ec321901-f077-4f71-a48c-20cae11c41d1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Área del visor principal{#main-viewer-area}

El área de vista principal es la zona ocupada por el video 360. Normalmente se configura para que se ajuste a la pantalla del dispositivo disponible cuando no se especifica ningún tamaño.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7video360viewer
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

## Ejemplo {#section-ee18025b182a42dc98052de5f133ddfe}

Para configurar un visor con un fondo blanco ( `#FFFFFF`) y lograr un tamaño de 512 x 288 píxeles.

```
.s7video360viewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

