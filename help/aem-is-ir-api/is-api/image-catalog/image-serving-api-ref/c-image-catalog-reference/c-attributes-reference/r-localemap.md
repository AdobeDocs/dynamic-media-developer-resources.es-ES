---
description: Mapa de traducción de ID. Especifica las reglas que se utilizan para traducir identificadores de imagen genéricos a ID específicos de configuración regional.
seo-description: Mapa de traducción de ID. Especifica las reglas que se utilizan para traducir identificadores de imagen genéricos a ID específicos de configuración regional.
seo-title: LocaleMap
solution: Experience Manager
title: LocaleMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LocaleMap{#localemap}

Mapa de traducción de ID. Especifica las reglas que se utilizan para traducir identificadores de imagen genéricos a ID específicos de configuración regional.

` *`elemento`*&#42;['|' *`elemento`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> elemento</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>ID de configuración regional (no distingue entre mayúsculas y minúsculas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Sufijo de configuración regional. </p></td> 
 </tr> 
</table>

`LocaleMap` hace referencia a un `locId` que se puede asignar a cualquier número de `locSuffix`.

Empty *`locSuffix`* values are permitted. *`locSuffix`* los valores deben ordenarse en el orden en que se buscarán. Se devuelve la primera coincidencia.

El servicio de imágenes busca en los *`locId`* valores una coincidencia sin distinción de mayúsculas y minúsculas con el `locale=` valor especificado en la solicitud. Si se encuentra una coincidencia, el primer valor asociado *`locSuffix`* se anexa a la ID del catálogo original. Si esta entrada de catálogo existe, se utiliza; de lo contrario, se prueba el siguiente *`locSuffix`* valor. Si ninguno de los *`locSuffix`* valores coincide con una entrada de catálogo, el servicio de imágenes devuelve un error o una imagen predeterminada.

Un valor vacío *`locId`* coincide con `locale=` cadenas vacías y desconocidas. Esto permite definir una regla predeterminada para configuraciones regionales desconocidas.

La traducción de ID, cuando está habilitada, se aplica a todos los identificadores que hacen referencia a las entradas del catálogo de imágenes y del catálogo de contenido estático.

## Propiedades {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Uno o varios elementos separados por|, donde cada elemento consta de dos o más valores de cadena separados por comas. *`locId`* y `locale=` se comparan. No distingue entre mayúsculas y minúsculas.

## Véase también {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Compatibilidad con Localización, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [atributo::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
