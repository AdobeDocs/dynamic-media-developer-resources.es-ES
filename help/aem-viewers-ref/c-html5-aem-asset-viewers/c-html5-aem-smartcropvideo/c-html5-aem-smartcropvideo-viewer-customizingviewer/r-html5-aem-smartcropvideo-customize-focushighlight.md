---
title: Enfoque destacado
description: El resaltado de enfoque de entrada que se muestra alrededor del elemento de interfaz de usuario del visor centrado se controla con el selector de clases CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 242b80db-f5b4-44ad-9169-bd6ecf859ed0
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
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
.s7smartcropvideoviewer *:focus
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

Ejemplo: para deshabilitar el resaltado de enfoque del explorador predeterminado para todos los elementos de la interfaz de usuario del visor, agregue el siguiente selector CSS a la hoja de estilo del visor:

```
.s7smartcropvideoviewer *:focus { 
 outline: none; 
}
```
