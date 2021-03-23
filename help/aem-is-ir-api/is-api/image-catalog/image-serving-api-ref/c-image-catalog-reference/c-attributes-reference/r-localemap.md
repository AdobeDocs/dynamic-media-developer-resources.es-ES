---
description: Mapa de traducción de ID. Especifica las reglas que se usan para traducir identificadores de imagen genéricos a identificadores específicos de configuración regional.
seo-description: Mapa de traducción de ID. Especifica las reglas que se usan para traducir identificadores de imagen genéricos a identificadores específicos de configuración regional.
seo-title: Mapa de configuración regional
solution: Experience Manager
title: Mapa de configuración regional
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---


# Mapa de configuración regional{#localemap}

Mapa de traducción de ID. Especifica las reglas que se usan para traducir identificadores de imagen genéricos a identificadores específicos de configuración regional.

`*``*&#42;['|' *`elemento de elemento`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> elemento</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>, <span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
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

`LocaleMap` hace referencia a una  `locId` que se puede asignar a cualquier número de  `locSuffix`.

Se permiten valores *`locSuffix`* vacíos. *`locSuffix`* Los valores deben ordenarse en el orden en que se buscarán. Se devuelve la primera coincidencia.

Image Serving busca en los valores *`locId`* una coincidencia que no distingue entre mayúsculas y minúsculas con el valor `locale=` especificado en la solicitud. Si se encuentra una coincidencia, el primer valor asociado *`locSuffix`* se anexa al ID de catálogo original. Si existe esta entrada de catálogo, se utiliza; de lo contrario, se intenta utilizar el siguiente valor *`locSuffix`*. Si ninguno de los valores *`locSuffix`* coincide con una entrada de catálogo, Image Serving devuelve un error o una imagen predeterminada.

Un valor *`locId`* vacío coincide con cadenas `locale=` vacías y desconocidas. Esto permite definir una regla predeterminada para configuraciones regionales desconocidas.

Cuando está habilitada, la traducción de ID se aplica a todos los id que hacen referencia a entradas del catálogo de imágenes y del catálogo de contenido estático.

## Propiedades {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Uno o más elementos separados por |, donde cada elemento consta de dos o más valores de cadena separados por coma. *`locId`* y  `locale=` se comparan. No distingue entre mayúsculas y minúsculas.

## Véase también {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Compatibilidad con localización, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [atributo::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
