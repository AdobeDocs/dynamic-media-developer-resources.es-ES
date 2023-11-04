---
description: Mapa de traducción de cadenas. Hace referencia a un locId que se puede asignar a cualquier número de internalLocId.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# LocaleStrMap{#localestrmap}

Mapa de traducción de cadenas. Hace referencia a un locId que se puede asignar a cualquier número de internalLocId.

`*`artículo`*&#42;['|' *`artículo`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> elemento </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Configuración regional (no distingue entre mayúsculas y minúsculas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>ID de configuración regional interna. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` hace referencia a un `locId` que se puede asignar a cualquier número de `internalLocId`.

Un vacío *`locale`* el valor coincide con vacío y desconocido `locale=` cadenas. Esto permite definir una regla predeterminada para configuraciones regionales desconocidas.

Empty *`locId`* Los valores de están permitidos y seleccione la opción *`defaultString`* (el *`defaultString`* no tiene un identificador de configuración regional). *`locId`* Los valores de se buscan en el orden especificado. Se devuelve la primera coincidencia.

Cuando la traducción de cadenas está habilitada, se aplica a las cadenas de texto en los siguientes campos del catálogo de imágenes:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Campo de catálogo</b> </td> 
   <td> <b>Elemento de cadena en el campo</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>Cualquier subelemento que contenga una cadena traducible (delimitado por cualquier combinación de separadores ',' ';' ':' o el inicio/final del campo). </p> <p>A <span class="codeph"> 0xrrggbb </span> el valor del color al principio de un campo localizable se excluye de la localización y se pasa sin modificaciones. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>Cualquier valor de atributo entre comillas simples o dobles, excepto los valores del atributo <span class="codeph"> coords= </span> y <span class="codeph"> shape= </span> atributos. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>El valor de cualquiera <span class="filepath"> objetivo.*.label </span> y <span class="filepath"> objetivo.*.userdata </span> propiedad. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>El valor de cualquier propiedad. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-8505a8525f6948ada3979f68c4081044}

Uno o más elementos, separados con |, donde cada elemento consta de dos o más valores de cadena separados por comas.

## Véase también {#section-0c0516e4f83d42d38247308cab9b6708}

Compatibilidad con localización, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
