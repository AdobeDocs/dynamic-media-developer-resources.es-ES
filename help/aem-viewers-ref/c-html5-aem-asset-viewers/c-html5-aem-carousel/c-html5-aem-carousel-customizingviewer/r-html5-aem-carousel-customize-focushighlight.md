---
description: El resaltado del foco de entrada que se muestra alrededor del elemento de interfaz de usuario del visualizador enfocado se controla con el selector de clases CSS.
solution: Experience Manager
title: Enfoque resaltado
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Developer,User
exl-id: f9343055-9fd9-4b19-bba3-1f742acb6193
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 1%

---

# Enfoque resaltado{#focus-highlight}

El resaltado del foco de entrada que se muestra alrededor del elemento de interfaz de usuario del visualizador enfocado se controla con el selector de clases CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS**

El aspecto se controla con el siguiente selector de clase CSS:

```
.s7carouselviewer *:focus
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
.s7carouselviewer *:focus { 
 outline: none; 
}
```
