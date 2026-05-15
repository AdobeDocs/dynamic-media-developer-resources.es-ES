---
description: Mapa de traducción de ID. Especifica las reglas utilizadas para traducir los ID de imagen genéricos a ID específicos de la configuración regional.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
TQID: 'https://experienceleague.adobe.com/LqHo03WC7EWKP7jt4l1X6kJffXcOQSd8unCxbdjOig4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 213
ht-degree: 0%

---

# LocaleMap{#localemap}

Mapa de traducción de ID. Especifica las reglas utilizadas para traducir los ID de imagen genéricos a ID específicos de la configuración regional.

`*`elemento`*&#42;['|' *`elemento`*]`

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

Se permiten valores *`locSuffix`* vacíos. *`locSuffix`* valores deben ordenarse en el orden en que se buscarán. Se devuelve la primera coincidencia.

El servicio de imágenes busca en los valores *`locId`* una coincidencia que no distingue entre mayúsculas y minúsculas con el valor `locale=` especificado en la solicitud. Si se encuentra una coincidencia, el primer valor *`locSuffix`* asociado se anexa al ID de catálogo original. Si existe esta entrada de catálogo, se utiliza; de lo contrario, se intenta el siguiente valor *`locSuffix`*. Si ninguno de los valores *`locSuffix`* coincide con una entrada de catálogo, el servicio de imágenes devuelve un error o una imagen predeterminada.

Un valor *`locId`* vacío coincide con cadenas `locale=` vacías y desconocidas. Esto permite definir una regla predeterminada para configuraciones regionales desconocidas.

Cuando la traducción de ID está habilitada, se aplica a todos los ID que hacen referencia a las entradas del catálogo de imágenes y del catálogo de contenido estático.

## Propiedades {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Uno o más elementos, separados con |, donde cada elemento consta de dos o más valores de cadena separados por comas. *`locId`* y `locale=` se comparan. No distingue entre mayúsculas y minúsculas.

## Véase también {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Compatibilidad con localización, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
