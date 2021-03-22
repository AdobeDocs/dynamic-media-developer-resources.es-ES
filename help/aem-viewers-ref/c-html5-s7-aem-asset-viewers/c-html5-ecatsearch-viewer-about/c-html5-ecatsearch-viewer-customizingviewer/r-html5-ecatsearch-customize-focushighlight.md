---
description: El resaltado del foco de entrada se muestra alrededor del elemento de interfaz de usuario del visualizador enfocado.
seo-description: El resaltado del foco de entrada se muestra alrededor del elemento de interfaz de usuario del visualizador enfocado.
seo-title: Enfoque resaltado
solution: Experience Manager
title: Enfoque resaltado
uuid: 0bd36795-e663-4f0e-8310-a57c2ffae4a2
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
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

