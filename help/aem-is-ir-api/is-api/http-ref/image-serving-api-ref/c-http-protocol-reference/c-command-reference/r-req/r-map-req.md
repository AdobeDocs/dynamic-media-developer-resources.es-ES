---
description: Datos del mapa de imágenes.
seo-description: Datos del mapa de imágenes.
seo-title: mapa
solution: Experience Manager
title: mapa
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 4%

---


# mapa{#map}

Datos del mapa de imágenes.

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificación</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador de solicitud única. </p></td> 
 </tr> 
</table>

Devuelve `catalog::Map` sin modificación al consultar una entrada de catálogo simple sin comandos adicionales especificados (no escalará a `catalog::maxPix`).

Si se especifica cualquier otro comando en la solicitud, se devuelve un mapa de imagen compuesto, que se deriva escalando, recortando, girando y capas todos los comandos `catalog::Map` y/o `map=` incluidos en la solicitud, tal como los datos de imagen estarían con `req=img`.

Especifique `text` u omita el segundo parámetro para devolver los datos del mapa de imagen en forma de una cadena de elemento `HTML <AREA>` con el tipo MIME de respuesta `text/plain`.

Especifique `xml` para dar formato a la respuesta como XML en lugar de HTML. La codificación de texto se puede especificar de forma opcional. El valor predeterminado es `UTF-8`.

Devuelve una cadena vacía (o un elemento `<AREA>` vacío) si no se encontraron datos de asignación para los objetos de catálogo especificados y/o si no quedan elementos `<AREA>` después de recortar las imágenes.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.

Consulte [Mapas de imágenes](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
