---
description: El resaltado de enfoque de entrada que se muestra alrededor del elemento de interfaz de usuario del visor enfocado se controla con el selector de clases CSS.
seo-description: El resaltado de enfoque de entrada que se muestra alrededor del elemento de interfaz de usuario del visor enfocado se controla con el selector de clases CSS.
seo-title: Resaltado de enfoque
solution: Experience Manager
title: Resaltado de enfoque
topic: Dynamic Media
uuid: 44057e10-98b6-4316-bf6c-9bf569be6a50
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---


# Resaltado de enfoque{#focus-highlight}

El resaltado de enfoque de entrada que se muestra alrededor del elemento de interfaz de usuario del visor enfocado se controla con el selector de clases CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades de CSS**

El aspecto se controla con el siguiente selector de clase CSS:

```
.s7interactivevideoviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> contorno  </span> </p> </td> 
   <td colname="col2"> <p>Estilo de resaltado de enfoque. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para desactivar el resaltado de enfoque predeterminado del navegador para todos los elementos de la interfaz de usuario del visor, agregue el siguiente selector CSS a la hoja de estilo del visor:

```
.s7interactivevideoviewer *:focus { 
 outline: none; 
}
```

