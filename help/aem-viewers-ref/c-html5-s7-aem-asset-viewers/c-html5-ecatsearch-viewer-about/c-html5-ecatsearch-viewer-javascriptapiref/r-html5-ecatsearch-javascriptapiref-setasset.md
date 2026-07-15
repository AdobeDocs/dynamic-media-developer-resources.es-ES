---
description: Referencia de la API de JavaScript para el visor de vídeo.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5fd80f8d-321e-47f4-9fb2-65e7bd63be58
TQID: 'https://experienceleague.adobe.com/lwSvqbGdXYM1txYvK2of-67envHzyEs4UMsnVmkPKj8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 1%

---

# setAsset{#setasset}

Referencia de la API de JavaScript para el visor de vídeo.

[!DNL ` setAsset( *`recurso`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recurso </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> cadena </span>} nuevo id de recurso o conjunto de imágenes explícito con modificadores opcionales del servicio de imágenes anexados después de <span class="codeph"> ? </span>. </p> <p> Las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content) no son compatibles con este visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

Establece un nuevo recurso. Puede llamar a este parámetro en cualquier momento, antes o después de [!DNL `init()`]. Si se llama después de [!DNL `init()`], el visor intercambia el recurso durante la ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referencia única a un conjunto de imágenes definido en un catálogo:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Conjunto de imágenes explícito, con páginas precombinadas:

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

