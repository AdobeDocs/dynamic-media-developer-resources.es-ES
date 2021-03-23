---
description: Referencia de la API de JavaScript para el visualizador de vídeo.
seo-description: Referencia de la API de JavaScript para el visualizador de vídeo.
seo-title: setAsset
solution: Experience Manager
title: setAsset
uuid: f106b3d4-880e-4ba3-ae47-a005af5c0f1b
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# setAsset{#setasset}

Referencia de la API de JavaScript para el visualizador de vídeo.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recurso  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Cadena </span>} nuevo id de recurso, conjunto de imágenes explícitas o conjunto de imágenes explícitas con modificadores de servicio de imágenes específicos de fotogramas, con modificadores de servicio de imágenes globales opcionales anexados después de "?". </p> <p> Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario). </p> </td> 
  </tr> 
 </tbody> 
</table>

Establece el nuevo recurso. Puede llamar a este parámetro en cualquier momento, ya sea antes o después de `init()`. Si se llama después de `init()`, el visor intercambia el recurso durante la ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referencia de imagen única:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Referencia única a un conjunto de imágenes definido en un catálogo:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Conjunto de imágenes explícito:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Conjunto de imágenes explícito con modificadores de servicio de imágenes específicos de fotogramas:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificador de enfoque añadido a todas las imágenes del conjunto:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```

