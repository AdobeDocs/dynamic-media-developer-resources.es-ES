---
description: El resaltado de enfoque de entrada se muestra alrededor del elemento de interfaz de usuario del visor seleccionado.
seo-description: El resaltado de enfoque de entrada se muestra alrededor del elemento de interfaz de usuario del visor seleccionado.
seo-title: Resaltado de enfoque
solution: Experience Manager
title: Resaltado de enfoque
topic: Dynamic media
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Resaltado de enfoque{#focus-highlight}

El resaltado de enfoque de entrada se muestra alrededor del elemento de interfaz de usuario del visor seleccionado.

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
   <td colname="col2"> <p> Estilo de resaltado de enfoque. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para desactivar el resaltado de enfoque predeterminado del navegador para todos los elementos de la interfaz de usuario del visor, agregue el siguiente selector CSS a la hoja de estilo del visor:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

