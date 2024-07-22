---
title: mapa
description: Datos de mapa de imagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

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
