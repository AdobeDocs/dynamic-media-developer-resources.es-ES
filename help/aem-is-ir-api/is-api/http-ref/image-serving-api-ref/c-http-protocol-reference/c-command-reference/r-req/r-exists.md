---
description: La imagen existe.
solution: Experience Manager
title: existe
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# existe{#exists}

La imagen existe.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* identificador de solicitud único

Devuelve una sola propiedad denominada `catalogRecord.exists`. El valor de la propiedad se establece en &quot;1&quot; si la entrada de catálogo especificada existe en la imagen o en el catálogo predeterminado; de lo contrario, se establece en &quot;0&quot;. `req=exists` solicitudes en el contexto `/is/content` indican la presencia o ausencia de un registro especificado en el catálogo de contenido estático.

Se omiten otros comandos de la cadena de solicitud. La respuesta HTTP se puede almacenar en caché con el TTL basado en `attribute::NonImgExpiration`.

Las solicitudes compatibles con el formato de respuesta JSONP le permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
