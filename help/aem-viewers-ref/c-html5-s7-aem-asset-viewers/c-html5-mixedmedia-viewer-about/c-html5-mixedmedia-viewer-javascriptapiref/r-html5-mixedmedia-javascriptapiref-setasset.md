---
title: setAsset
description: Referencia de la API de JavaScript para el visualizador de medios mixtos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# setAsset{#setasset}

Referencia de la API de JavaScript para el visualizador de medios mixtos.

` setAsset( *`recurso`*[,data]))`

Establece el nuevo recurso y los datos de recurso adicionales opcionales. Puede llamar a este parámetro en cualquier momento, antes o después de `init()`. Si se llama después de `init()`, el visor intercambia el recurso durante la ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parámetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`recurso`*` - { `String`} nuevo ID de recurso o conjunto de medios mixtos explícito, con modificadores opcionales del servicio de imágenes anexados después de `?`.

Las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content) no son compatibles con este visor.

`*`datos`*` - {`JSON`} ubicación del nuevo archivo de subtítulos.

Si no se especifica, el botón de título no estará visible en la interfaz de usuario. Los subtítulos especificados con este parámetro se aplican al vídeo que aparece primero en el conjunto de medios mixtos; los vídeos posteriores se reproducen sin subtítulos. Este visor es compatible con los siguientes ID de componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID de componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nombre de clase de componente de SDK de visor </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de póster </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se mostrará en el primer fotograma antes de que comience la reproducción del vídeo. </p> <p>Ver <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pie de ilustración </span> </p> </td> 
   <td colname="col2"> <p> Ubicación del nuevo archivo de rótulo. </p> <p>Si no se especifica, el botón de título no estará visible en la interfaz de usuario. Los subtítulos especificados con este parámetro se aplican al vídeo que aparece primero en el conjunto de medios. Los vídeos posteriores se reproducen sin subtítulos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referencia de conjunto de medios único:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Conjunto de medios explícito:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Modificador de enfoque añadido a todas las imágenes del conjunto:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```
