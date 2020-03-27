---
description: Referencia de la API de JavaScript para el visor de zoom básico.
seo-description: Referencia de la API de JavaScript para el visor de zoom básico.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: af433f15-34a0-4867-97c5-acab47e3e008
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

Referencia de la API de JavaScript para el visor de zoom básico.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recurso</span></span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Cadena</span>} nueva ID de recurso, con modificadores IS opcionales anexados después de "?" </p> <p> Este visor no admite las imágenes que usan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario). </p> </td> 
  </tr> 
 </tbody> 
</table>

Establece el nuevo recurso. Puede llamar a este parámetro en cualquier momento, ya sea antes o después `init()`. Si se llama después `init()`, el visor intercambia el recurso en tiempo de ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referencia de una sola imagen:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Modificador de enfoque añadido a todas las imágenes del conjunto:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```

