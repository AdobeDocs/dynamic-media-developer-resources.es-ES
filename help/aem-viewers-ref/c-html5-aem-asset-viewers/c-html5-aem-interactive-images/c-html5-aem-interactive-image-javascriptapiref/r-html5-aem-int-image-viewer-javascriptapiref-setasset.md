---
description: Referencia de la API de JavaScript para el visor de imágenes de vídeo.
seo-description: Referencia de la API de JavaScript para el visor de imágenes de vídeo.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 8cb10b2e-addb-4659-a93b-5a53d0f8a5bb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---


# setAsset{#setasset}

Referencia de la API de JavaScript para el visor de imágenes de vídeo.

` setAsset( *`asset`*)`

Establece el nuevo recurso. Puede llamar a este parámetro en cualquier momento, ya sea antes o después de `init()`. Si se llama después de `init()`, el visor intercambia el recurso en tiempo de ejecución.

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recurso</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nuevo ID de recurso. </p> <p>Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referencia de una sola imagen:

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```

