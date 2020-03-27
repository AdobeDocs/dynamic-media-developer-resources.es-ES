---
description: La imagen existe.
seo-description: La imagen existe.
seo-title: existe
solution: Experience Manager
title: existe
topic: Scene7 Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# existe{#exists}

La imagen existe.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* identificador de solicitud único

Devuelve una única propiedad denominada `catalogRecord.exists`. El valor de la propiedad se establece en &quot;1&quot; si la entrada de catálogo especificada existe en la imagen o en el catálogo predeterminado; de lo contrario, se establece en &quot;0&quot;. `req=exists` las solicitudes con respecto al `/is/content` contexto indicarán la presencia o ausencia de un registro especificado en el catálogo de contenido estático.

Se omiten otros comandos de la cadena de solicitud. The HTTP response is cacheable with the TTL based on `attribute::NonImgExpiration`.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del `req=` parámetro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
