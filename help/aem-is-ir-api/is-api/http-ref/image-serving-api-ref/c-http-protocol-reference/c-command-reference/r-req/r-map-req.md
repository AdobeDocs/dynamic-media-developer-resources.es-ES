---
description: Datos del mapa de imagen.
seo-description: Datos del mapa de imagen.
seo-title: mapa
solution: Experience Manager
title: mapa
topic: Scene7 Image Serving - Image Rendering API
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 4%

---


# mapa{#map}

Datos del mapa de imagen.

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificación</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador de solicitud único. </p></td> 
 </tr> 
</table>

Devuelve `catalog::Map` sin modificación al consultar una entrada de catálogo simple sin comandos adicionales especificados (no se escalará a `catalog::maxPix`).

Si se especifica cualquier otro comando en la solicitud, se devuelve un mapa de imagen compuesto, que se deriva escalando, recortando, rotando y superponiendo todos los comandos `catalog::Map` y/o `map=` incluidos en la solicitud, del mismo modo que los datos de imagen se obtendrían con `req=img`.

Especifique `text` u omita el segundo parámetro para devolver los datos del mapa de imagen en forma de una cadena de elemento `HTML <AREA>` con tipo MIME de respuesta `text/plain`.

Especifique `xml` para dar formato a la respuesta como XML en lugar de HTML. La codificación de texto se puede especificar de forma opcional. El valor predeterminado es `UTF-8`.

Devuelve una cadena vacía (o un elemento vacío `<AREA>`) si no se encontraron datos de mapa para los objetos de catálogo especificados y/o si no quedan elementos `<AREA>` después de recortar las imágenes.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.

Consulte [Mapas de imagen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
