---
description: Versiones disponibles específicas de la configuración regional. Devuelve una lista de versiones disponibles específicas de la configuración regional del id de catálogo especificado en la ruta de solicitud.
solution: Experience Manager
title: xlate
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: bf5b3cb7-9792-4eca-a1aa-55aa4089b4d4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# xlate{#xlate}

Versiones disponibles específicas de la configuración regional. Devuelve una lista de versiones disponibles específicas de la configuración regional del id de catálogo especificado en la ruta de solicitud.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificador de solicitud única. </p></td> 
 </tr> 
</table>

Consulte [Traducción de Id de objeto](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

Por ejemplo:

`xlate.translatedIds=image,image_fr,image_de`

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
