---
description: Referencia de la API de JavaScript para el visor de medios mixtos.
seo-description: Referencia de la API de JavaScript para el visor de medios mixtos.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 8c341a8a-25b5-4db9-ad1a-919ded79f2ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# setAsset{#setasset}

Referencia de la API de JavaScript para el visor de medios mixtos.

` setAsset( *`asset`*[,data]))`

Establece el nuevo recurso y los datos adicionales opcionales del recurso. Puede llamar a este parámetro en cualquier momento, ya sea antes o después de `init()`. Si se llama después de `init()`, el visor intercambia el recurso en tiempo de ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parámetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`recurso`*` : { `String`} nuevo ID de recurso o conjunto de medios mixtos explícito, con los modificadores opcionales de servicio de imágenes añadidos después  `?`.

Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario).

` *`data`*` - { `JSON`} ubicación del nuevo archivo de rótulo.

Si no se especifica, el botón de rótulo no está visible en la interfaz de usuario. Los rótulos especificados con este parámetro se aplican al vídeo que aparece primero en el conjunto de medios mixtos; los vídeos subsiguientes se reproducen sin rótulos. Este visor admite los siguientes ID de componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID del componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nombre de clase de componente del SDK de visor </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage  </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra en el primer fotograma antes de que se reproduzca el inicio del vídeo. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> caption  </span> </p> </td> 
   <td colname="col2"> <p> Ubicación del nuevo archivo de subtítulos. </p> <p>Si no se especifica, el botón de rótulo no está visible en la interfaz de usuario. Los rótulos especificados con este parámetro se aplican al vídeo que aparece primero en el conjunto de medios. Los vídeos posteriores se reproducen sin subtítulos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referencia de conjunto de medios únicos:

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

