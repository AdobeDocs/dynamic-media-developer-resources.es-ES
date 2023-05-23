---
title: Enfoque destacado
description: El resaltado de enfoque de entrada que se muestra alrededor del elemento de interfaz de usuario del visor centrado se controla con el selector de clases CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 31fd8022-0072-4a4c-8947-57858a094f3c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# Enfoque destacado{#focus-highlight}

El resaltado de enfoque de entrada que se muestra alrededor del elemento de interfaz de usuario del visor centrado se controla con el selector de clases CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades de CSS**

El aspecto se controla con el siguiente selector de clase CSS:

```
.s7zoomviewer *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contorno </span> </p> </td> 
   <td colname="col2"> <p>Estilo de resalte de enfoque. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para deshabilitar el resaltado de enfoque del explorador predeterminado para todos los elementos de la interfaz de usuario del visor, agregue el siguiente selector CSS a la hoja de estilo del visor:

```
.s7zoomviewer *:focus { 
 outline: none; 
}
```
