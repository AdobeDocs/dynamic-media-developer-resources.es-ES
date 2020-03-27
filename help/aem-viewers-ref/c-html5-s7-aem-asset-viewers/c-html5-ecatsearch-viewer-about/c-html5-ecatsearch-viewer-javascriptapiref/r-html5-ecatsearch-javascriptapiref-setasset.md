---
description: Referencia de la API de JavaScript para el visor de vídeos.
seo-description: Referencia de la API de JavaScript para el visor de vídeos.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: ab078f32-c523-4b6c-a0d6-45dd2af35b36
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setAsset{#setasset}

Referencia de la API de JavaScript para el visor de vídeos.

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recurso </span></span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Cadena </span>} nueva identificación de recurso o conjunto de imágenes explícito con los modificadores opcionales de servicio de imágenes añadidos después de <span class="codeph"> ? </span>. </p> <p> Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario). </p> </td> 
  </tr> 
 </tbody> 
</table>

Define un nuevo recurso. Puede llamar a este parámetro en cualquier momento, ya sea antes o después [!DNL `init()`]. Si se llama después [!DNL `init()`], el visor intercambia el recurso en tiempo de ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referencia única a un conjunto de imágenes definido en un catálogo:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Conjunto de imágenes explícito, con páginas previamente combinadas:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Conjunto de imágenes explícitas, con imágenes de página individuales:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Modificador de enfoque añadido a todas las imágenes del conjunto:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

