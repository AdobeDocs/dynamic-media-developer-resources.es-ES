---
description: ID de configuración regional de traducción. Especifica el ID de configuración regional para la solicitud.
seo-description: ID de configuración regional de traducción. Especifica el ID de configuración regional para la solicitud.
seo-title: configuración regional
solution: Experience Manager
title: configuración regional
topic: Scene7 Image Serving - Image Rendering API
uuid: 82acc0bb-fd94-44c9-8ff9-3b9cefab4627
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# locale{#locale}

ID de configuración regional de traducción. Especifica el ID de configuración regional para la solicitud.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>ID de configuración regional (cadena). </p></td> 
 </tr> 
</table>

Utilizando este ID y las reglas especificadas con `attribute::LocaleMap` y `attribute::LocaleStrMap`, el servicio de imágenes aplica localización opcional de cadena y traducción de ID de catálogo.

## Propiedades {#section-1854a9902b884d9b8e8e713b6635723f}

Solicitar. Se aplica a toda la solicitud, incluidas las solicitudes anidadas o incrustadas, independientemente de dónde se haya especificado. `locId` solo debe incluir caracteres ASCII imprimibles. Se omite si no hay mapas de localización definidos en el catálogo principal de esta solicitud. Se devuelve un error si `locId` se especifica vacío o no válido y no se define ninguna regla predeterminada en `attribute::DefaultLocale`.

## Predeterminado {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` se utiliza cuando no se especifica locale=.

## Véase también {#section-28a586d43ac4429d98e318a580c92af4}

[atributo::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [atributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [atributo::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), compatibilidad con Localizaciones
