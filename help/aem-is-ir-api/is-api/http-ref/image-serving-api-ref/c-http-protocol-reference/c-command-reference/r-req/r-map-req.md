---
title: mapa
description: Datos de mapa de imagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
TQID: 'https://experienceleague.adobe.com/Ly1JWjeEyZWUEiyVcv-t-OKf0cp6uuMsbR0B6BE1fhY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 224
ht-degree: 1%

---

# mapa{#map}

Datos de mapa de imagen.

`req=map[,text|{xml[, *`codificación`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificación</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador único de la solicitud. </p></td> 
 </tr> 
</table>

Devuelve `catalog::Map` sin modificaciones al consultar una entrada de catálogo simple sin comandos adicionales especificados (no se escala a `catalog::maxPix`).

Si se especifican otros comandos en la solicitud, se devuelve un mapa de imagen compuesto. El mapa de imagen compuesto se deriva escalando, recortando, girando y superponiendo en capas todos los comandos `catalog::Map` o `map=` incluidos en la solicitud, tal como lo harían los datos de imagen con `req=img`.

Especifique `text` u omita el segundo parámetro para que pueda devolver los datos del mapa de imagen en forma de cadena de elemento `HTML <AREA>` con el tipo MIME de respuesta `text/plain`.

Especifique `xml` para que pueda dar formato a la respuesta como XML en lugar de como HTML. Se puede especificar la codificación de texto de forma opcional. El valor predeterminado es `UTF-8`.

Devuelve una cadena vacía (o un elemento `<AREA>` vacío) si no se encontraron datos de asignación para los objetos de catálogo especificados o si no queda ningún elemento `<AREA>` después de recortar las imágenes.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.

Las solicitudes compatibles con el formato de respuesta JSONP le permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.

Ver [mapas de imagen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
