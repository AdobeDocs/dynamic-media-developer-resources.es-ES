---
title: Enfoque resaltado
description: El resaltado del foco de entrada que se muestra alrededor del elemento de interfaz de uso del visor enfocado se controla con el selector de clases CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 74ff9669-d56b-4731-9d4a-dda7c831e162
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# Enfoque resaltado{#focus-highlight}

El resaltado del foco de entrada que se muestra alrededor del elemento de interfaz de uso del visor enfocado se controla con el selector de clases CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto se controla con el siguiente selector de clase CSS:

```
.s7basiczoomviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> descripción </span> </p> </td> 
   <td colname="col2"> <p>Estilo de resaltado de enfoque. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para desactivar el resaltado de enfoque predeterminado del navegador para todos los elementos de la interfaz de usuario del visor, añada el siguiente selector CSS a la hoja de estilos del visor:

```
.s7basiczoomviewer *:focus { 
 outline: none; 
}
```
