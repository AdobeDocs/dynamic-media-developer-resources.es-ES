---
title: Enfoque destacado
description: Resalte de enfoque de entrada mostrado alrededor del elemento de interfaz de usuario del visor enfocado.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# Enfoque destacado{#focus-highlight}

Resalte de enfoque de entrada mostrado alrededor del elemento de interfaz de usuario del visor enfocado.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

El aspecto del resaltado de enfoque se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer *:focus
```

**Propiedades CSS del resaltado de enfoque**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contorno </span> </p> </td> 
   <td colname="col2"> <p> Estilo de resalte de enfoque. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para deshabilitar el resaltado de enfoque del explorador predeterminado para todos los elementos de la interfaz de usuario del visor, agregue el siguiente selector CSS a la hoja de estilo del visor:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
