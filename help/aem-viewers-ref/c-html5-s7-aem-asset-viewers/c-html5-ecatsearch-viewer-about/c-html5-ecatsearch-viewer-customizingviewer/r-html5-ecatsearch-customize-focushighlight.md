---
description: El resaltado del foco de entrada se muestra alrededor del elemento de interfaz de usuario del visualizador enfocado.
solution: Experience Manager
title: Enfoque resaltado
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Developer,Business Practitioner
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# Enfoque resaltado{#focus-highlight}

El resaltado del foco de entrada se muestra alrededor del elemento de interfaz de usuario del visualizador enfocado.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

El aspecto del resaltado de enfoque se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer *:focus
```

**Propiedades CSS del resaltado del enfoque**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> descripción  </span> </p> </td> 
   <td colname="col2"> <p> Estilo de resaltado de enfoque. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para desactivar el resaltado de enfoque predeterminado del navegador para todos los elementos de la interfaz de usuario del visor, añada el siguiente selector CSS a la hoja de estilos del visor:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
