---
description: Los datos de imagen se devuelven si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req=img o req=tmb.
seo-description: Los datos de imagen se devuelven si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req=img o req=tmb.
seo-title: Imágenes
solution: Experience Manager
title: Imágenes
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# Imágenes{#images}

Los datos de imagen se devuelven si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req=img o req=tmb.

El tipo MIME de respuesta HTTP está determinado por `fmt=` o, si `fmt=` no se especifica, es `<image/jpeg>`.

El estado de la respuesta HTTP es &#39;200 OK&#39; si el método de solicitud es incondicional `GET` o `HEAD`.

El servidor puede responder con el estado &quot;304&quot; (no modificado) y no devolver ningún dato de imagen en respuesta a una solicitud condicional `GET` (que incluye un encabezado `If-Modified-Since` o `If-None-Match` válido).
