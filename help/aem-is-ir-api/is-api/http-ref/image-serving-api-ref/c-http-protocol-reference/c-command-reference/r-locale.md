---
title: configuración regional
description: ID de configuración regional de traducción. Especifica el ID de configuración regional de la solicitud.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
TQID: 'https://experienceleague.adobe.com/VTRopZpc1aMPvWk3QRd0XyAVf-y782AVidiSDiuYdKM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 119
ht-degree: 4%

---

# configuración regional{#locale}

ID de configuración regional de traducción. Especifica el ID de configuración regional de la solicitud.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>ID local (cadena). </p></td> 
 </tr> 
</table>

Con este id. y las reglas especificadas con `attribute::LocaleMap` y `attribute::LocaleStrMap`, el servicio de imágenes aplica la traducción del id. de catálogo y la localización de cadenas opcionales.

## Propiedades {#section-1854a9902b884d9b8e8e713b6635723f}

Solicitar comando. Se aplica a toda la solicitud, incluidas las solicitudes anidadas/incrustadas, independientemente de dónde se especifique. `locId` solo debe incluir caracteres ASCII imprimibles. Se ignora si no se definen mapas de localización en el catálogo principal de esta solicitud. Se devuelve un error si se especifica `locId` vacío o no válido y no se define ninguna regla predeterminada en `attribute::DefaultLocale`.

## Predeterminado {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` se usa cuando locale= no se especifica.

## Véase también {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), compatibilidad con la localización
