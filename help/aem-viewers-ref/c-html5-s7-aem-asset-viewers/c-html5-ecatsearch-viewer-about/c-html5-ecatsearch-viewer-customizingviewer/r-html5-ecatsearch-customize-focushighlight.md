---
title: Enfoque destacado
description: Resalte de enfoque de entrada mostrado alrededor del elemento de interfaz de usuario del visor enfocado.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
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

Por ejemplo, para deshabilitar el resaltado de enfoque del explorador predeterminado para todos los elementos de la interfaz de usuario del visor, agregue el siguiente selector CSS a la hoja de estilo del visor:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
