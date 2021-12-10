---
title: setAsset
description: Referencia de la API de JavaScript para el visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# setAsset{#setasset}

Referencia de la API de JavaScript para el visualizador de vídeo.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recurso </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Cadena </span>} nuevo id de recurso, conjunto de imágenes explícito o conjunto de imágenes explícito con modificadores de Image Serving específicos del marco, con modificadores opcionales globales de Image Serving anexados después de "?". </p> <p> Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario). </p> </td> 
  </tr> 
 </tbody> 
</table>

Establece el nuevo recurso. Puede llamar a este parámetro en cualquier momento, ya sea antes o después de `init()`. Si se llama después de `init()`, el visor intercambia el recurso durante la ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referencia de imagen única como se indica a continuación:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Una única referencia a un conjunto de imágenes que se define en un catálogo de la siguiente manera:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

La imagen explícita se establece de la siguiente manera:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Conjunto de imágenes explícito con modificadores de Image Serving específicos del marco de la siguiente manera:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificador de enfoque añadido a todas las imágenes del conjunto de la siguiente manera:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
