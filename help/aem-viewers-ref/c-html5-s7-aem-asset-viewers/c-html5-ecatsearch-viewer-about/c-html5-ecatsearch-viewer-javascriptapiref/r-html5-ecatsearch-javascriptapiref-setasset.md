---
description: Referencia de la API de JavaScript para el visualizador de vídeo.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# setAsset{#setasset}

Referencia de la API de JavaScript para el visualizador de vídeo.

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recurso  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Cadena </span>} nuevo id de recurso o conjunto de imágenes explícito con modificadores opcionales de servicio de imágenes anexados después de <span class="codeph"> ? </span>. </p> <p> Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario). </p> </td> 
  </tr> 
 </tbody> 
</table>

Define un nuevo recurso. Puede llamar a este parámetro en cualquier momento, ya sea antes o después de [!DNL `init()`]. Si se llama después de [!DNL `init()`], el visor intercambia el recurso durante la ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referencia única a un conjunto de imágenes definido en un catálogo:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Conjunto de imágenes explícito, con páginas combinadas previamente:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Conjunto de imágenes explícito, con imágenes de página individuales:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Modificador de enfoque añadido a todas las imágenes del conjunto:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

