---
title: setAsset
description: Referencia de la API de JavaScript para el visor flotante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: cd66267e-7b25-4af4-b83c-f7b7f768ea8c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# setAsset{#setasset}

Referencia de la API de JavaScript para el visor flotante.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recurso</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Cadena</span>} nuevo id de recurso, conjunto de imágenes explícito o conjunto de imágenes explícito con modificadores de servicio de imágenes específicos de fotograma, con modificadores globales de servicio de imágenes opcionales anexados después de <span class="codeph"> ?</span>. </p> <p> Las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content) no son compatibles con este visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

Establece el nuevo recurso. Puede llamar a este parámetro en cualquier momento, antes o después de `init()`. Si se llama después de `init()`, el visor intercambia el recurso durante la ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

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

Imagen explícita establecida de la siguiente manera:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Conjunto de imágenes explícito con modificadores de servicio de imágenes específicos de marcos:

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificador de enfoque añadido a todas las imágenes del conjunto:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
