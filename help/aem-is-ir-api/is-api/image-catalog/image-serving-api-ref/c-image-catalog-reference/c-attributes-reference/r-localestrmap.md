---
description: Mapa de traducción de cadenas. Hace referencia a un locId que se puede asignar a cualquier número de internalLocId.
seo-description: Mapa de traducción de cadenas. Hace referencia a un locId que se puede asignar a cualquier número de internalLocId.
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 1%

---


# LocaleStrMap{#localestrmap}

Mapa de traducción de cadenas. Hace referencia a un locId que se puede asignar a cualquier número de internalLocId.

`*``*&#42;['|' *`elemento de elemento`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> elemento </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> configuración regional  </span>,  <span class="varname"> locId  </span>*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Configuración regional (sin distinción de mayúsculas y minúsculas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>ID de configuración regional interna. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` hace referencia a una  `locId` que se puede asignar a cualquier número de  `internalLocId`.

Un valor *`locale`* vacío coincide con cadenas `locale=` vacías y desconocidas. Esto permite definir una regla predeterminada para configuraciones regionales desconocidas.

Se permiten valores *`locId`* vacíos y seleccione *`defaultString`* (el *`defaultString`* no tiene un identificador de configuración regional). *`locId`* se buscan en el orden especificado. Se devuelve la primera coincidencia.

La traducción de cadenas, cuando está habilitada, se aplica a cadenas de texto en los siguientes campos de catálogo de imágenes:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Campo de catálogo</b> </td> 
   <td> <b>Elemento Cadena en el campo</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::ImageSet  </span> </p> </td> 
   <td> <p>Cualquier subelemento que contenga una cadena traducible (delimitado por cualquier combinación de separadores ',' ';' ':' y/o el inicio/final del campo). </p> <p>Un valor de color <span class="codeph"> 0xrrgbb </span> al principio de un campo localizable se excluye de la localización y se transfiere sin modificaciones. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Map  </span> </p> </td> 
   <td> <p>Cualquier valor de atributo entre comillas simples o dobles, excepto los valores de los atributos <span class="codeph"> coords= </span> y <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Targets  </span> </p> </td> 
   <td> <p>El valor de cualquier destinatario <span class="filepath">.Destino *.label </span> y <span class="filepath">.*.userdata </span> propiedad. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::UserData  </span> </p> </td> 
   <td> <p>El valor de cualquier propiedad. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-8505a8525f6948ada3979f68c4081044}

Uno o más elementos separados por |, donde cada elemento consta de dos o más valores de cadena separados por coma.

## Véase también {#section-0c0516e4f83d42d38247308cab9b6708}

Compatibilidad con localización, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [atributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catálogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catálogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catálogo::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catálogo::UserData&lt;a 11/>](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
