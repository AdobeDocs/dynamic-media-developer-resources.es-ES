---
description: La imagen existe.
seo-description: La imagen existe.
seo-title: existe
solution: Experience Manager
title: existe
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 4%

---


# existe{#exists}

La imagen existe.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* identificador único de solicitud

Devuelve una sola propiedad denominada `catalogRecord.exists`. El valor de la propiedad se establece en &quot;1&quot; si la entrada de catálogo especificada existe en la imagen o en el catálogo predeterminado; de lo contrario, se establece en &quot;0&quot;. `req=exists` las solicitudes en el  `/is/content` contexto indican la presencia o ausencia de un registro especificado en el catálogo de contenido estático.

Se omiten otros comandos de la cadena de solicitud. La respuesta HTTP se puede almacenar en caché con el TTL basado en `attribute::NonImgExpiration`.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
