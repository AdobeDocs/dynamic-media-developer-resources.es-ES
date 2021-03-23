---
description: El resaltado del foco de entrada que se muestra alrededor del elemento de interfaz de uso del visor enfocado se controla con el selector de clases CSS.
seo-description: El resaltado del foco de entrada que se muestra alrededor del elemento de interfaz de uso del visor enfocado se controla con el selector de clases CSS.
seo-title: Enfoque resaltado
solution: Experience Manager
title: Enfoque resaltado
uuid: 1b552aec-837a-4df4-91dc-615ceead92b3
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

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
   <td colname="col1"> <p> <span class="codeph"> descripción  </span> </p> </td> 
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

