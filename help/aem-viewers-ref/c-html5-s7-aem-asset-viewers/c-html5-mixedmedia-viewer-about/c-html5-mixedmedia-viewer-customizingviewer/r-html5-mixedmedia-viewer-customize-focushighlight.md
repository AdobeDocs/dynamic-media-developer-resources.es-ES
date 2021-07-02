---
description: El resaltado del foco de entrada que se muestra alrededor del elemento de la interfaz de usuario del visor centrado se controla con el selector de clases CSS.
solution: Experience Manager
title: Enfoque resaltado
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de medios mixtos
role: Developer,Business Practitioner
exl-id: 7d29dab2-6f01-4328-9e92-0c370acaa2d6
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---

# Enfoque resaltado{#focus-highlight}

El resaltado del foco de entrada que se muestra alrededor del elemento de la interfaz de usuario del visor centrado se controla con el selector de clases CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS**

El aspecto se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> descripción  </span> </p> </td> 
   <td colname="col2"> <p>Estilo de resaltado de enfoque. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para desactivar el resaltado de enfoque predeterminado del navegador para todos los elementos de la interfaz de usuario del visor, añada el siguiente selector CSS a la hoja de estilos del visor:

```
.s7mixedmediaviewer *:focus { 
 outline: none; 
}
```
