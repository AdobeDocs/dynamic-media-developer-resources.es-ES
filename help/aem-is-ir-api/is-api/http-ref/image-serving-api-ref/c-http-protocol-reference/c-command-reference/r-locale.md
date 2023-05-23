---
description: ID de configuración regional de traducción. Especifica el ID de configuración regional de la solicitud.
solution: Experience Manager
title: configuración regional
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
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

Usar este ID y las reglas especificadas con `attribute::LocaleMap` y `attribute::LocaleStrMap`, el servicio de imágenes aplica la traducción del ID de catálogo y la localización de cadenas opcionales.

## Propiedades {#section-1854a9902b884d9b8e8e713b6635723f}

Solicitar comando. Se aplica a toda la solicitud, incluidas las solicitudes anidadas/incrustadas, independientemente de dónde se especifique. `locId` solo debe incluir caracteres ASCII imprimibles. Se ignora si no se definen mapas de localización en el catálogo principal de esta solicitud. Se devuelve un error si está vacío o no es válido `locId` se ha especificado y no se ha definido ninguna regla predeterminada en `attribute::DefaultLocale`.

## Predeterminado {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` se utiliza cuando locale= no se especifica.

## Véase también {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Compatibilidad con localización
