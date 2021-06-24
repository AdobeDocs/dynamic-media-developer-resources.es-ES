---
description: Referencia de la API de JavaScript para el visor de carrusel.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Developer,Business Practitioner
exl-id: e8aaee4e-56d5-46e4-8499-d5c9a6ba5d3b
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 3%

---

# setAsset{#setasset}

Referencia de la API de JavaScript para el visor de carrusel.

` setAsset( *`asset`*)`

Establece el nuevo recurso. Puede llamar a este parámetro en cualquier momento, ya sea antes o después de `init()`. Si se llama después de `init()`, el visor intercambia el recurso durante la ejecución.

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recurso</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Cadena</span>} nuevo ID de recurso. </p> <p>Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referencia de imagen única:

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```
