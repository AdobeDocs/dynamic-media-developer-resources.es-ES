---
title: Área del visor principal
description: El área de vista principal está ocupada por el vídeo de recorte inteligente. Normalmente se configura para que se ajuste a la pantalla de dispositivo disponible cuando no se especifica ningún tamaño.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 7d1379c1-7746-4f61-92df-e8ac4ab7d506
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# Área del visor principal{#main-viewer-area}

El área de vista principal está ocupada por el vídeo. Normalmente se configura para que se ajuste a la pantalla de dispositivo disponible cuando no se especifica ningún tamaño.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El siguiente selector de clase CSS controla el aspecto del área de visualización:

```
.s7smartcropvideoviewer 
```

## Propiedades CSS del área principal del visor {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo en formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar un visualizador de vídeo de recorte inteligente con un fondo blanco (#FFFFFF) y definir su tamaño 512 x 288 píxeles:

```
.s7smartcropvideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
