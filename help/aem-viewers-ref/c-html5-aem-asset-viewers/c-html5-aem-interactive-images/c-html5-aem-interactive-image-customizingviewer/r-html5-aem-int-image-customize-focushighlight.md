---
title: Enfoque destacado
description: El resaltado de enfoque de entrada que se muestra alrededor del elemento de interfaz de usuario del visor centrado se controla con el selector de clases CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 89f34a96-2b21-4169-8c25-4b53005e59b8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
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
.s7interactiveimage *:focus
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
.s7interactiveimage *:focus { 
 outline: none; 
}
```
