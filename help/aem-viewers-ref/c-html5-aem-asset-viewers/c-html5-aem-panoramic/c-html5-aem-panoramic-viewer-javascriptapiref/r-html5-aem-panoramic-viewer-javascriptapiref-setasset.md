---
title: setAsset
description: Referencia de la API de JavaScript para el visor panorámico.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
autotag-review: '2026-05-13T22:10:13.118Z'
TQID: 'https://experienceleague.adobe.com/r2jI4YcDd17kY1Zn1U9QHqr3e9Ea9-S8YPwkaK66gPI'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 2%

---

# setAsset{#setasset}

Referencia de la API de JavaScript para el visor panorámico.

`setAsset(asset)`

Establece el nuevo recurso. Puede llamar a este parámetro en cualquier momento, antes o después de `init()`. Si se llama después de `init()`, el visor intercambia el recurso durante la ejecución.

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-javascriptapiref/r-html5-aem-panoramic-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> recurso </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> cadena</span>} id. de recurso nuevo. Este visor no admite imágenes que utilicen procesamiento de imágenes (IR) o contenido generado por el usuario (UGC). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/PanoramicImage-Sample")
```
