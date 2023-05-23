---
description: Mapa de traducción de ID. Especifica las reglas utilizadas para traducir los ID de imagen genéricos a ID específicos de la configuración regional.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---

# LocaleMap{#localemap}

Mapa de traducción de ID. Especifica las reglas utilizadas para traducir los ID de imagen genéricos a ID específicos de la configuración regional.

`*`artículo`*&#42;['|' *`artículo`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> elemento</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>ID de configuración regional (sin distinción de mayúsculas y minúsculas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Sufijo de configuración regional. </p></td> 
 </tr> 
</table>

`LocaleMap` hace referencia a un `locId` que se puede asignar a cualquier número de `locSuffix`.

Empty *`locSuffix`* Los valores de están permitidos. *`locSuffix`* Los valores de deben ordenarse en el orden en que se buscarán. Se devuelve la primera coincidencia.

El servicio de imágenes busca en *`locId`* valores para una coincidencia sin distinción entre mayúsculas y minúsculas con `locale=` valor especificado en la solicitud. Si se encuentra una coincidencia, la primera asociada *`locSuffix`* el valor se añade al id de catálogo original. Si existe esta entrada de catálogo, se utiliza; de lo contrario, la siguiente *`locSuffix`* se intenta el valor. Si ninguno de los *`locSuffix`* Si los valores coinciden con una entrada de catálogo, el servicio de imágenes devuelve un error o una imagen predeterminada.

Un vacío *`locId`* el valor coincide con vacío y desconocido `locale=` cadenas. Esto permite definir una regla predeterminada para configuraciones regionales desconocidas.

Cuando la traducción de ID está habilitada, se aplica a todos los ID que hacen referencia a las entradas del catálogo de imágenes y del catálogo de contenido estático.

## Propiedades {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Uno o más elementos, separados con |, donde cada elemento consta de dos o más valores de cadena separados por comas. *`locId`* y `locale=` se comparan. No distingue mayúsculas de minúsculas.

## Véase también {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Compatibilidad con localización, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
