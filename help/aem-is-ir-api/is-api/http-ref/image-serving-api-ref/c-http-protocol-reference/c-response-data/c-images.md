---
description: Se devuelven datos de imagen si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req=img o req=tmb.
solution: Experience Manager
title: Imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---

# Imágenes{#images}

Se devuelven datos de imagen si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req=img o req=tmb.

El tipo MIME de respuesta HTTP está determinado por `fmt=` o, si no se especifica `fmt=`, es `<image/jpeg>`.

El estado de la respuesta HTTP es &#39;200 OK&#39; si el método de solicitud era un `GET` o `HEAD` incondicional.

El servidor puede responder con el estado &quot;304&quot; (no modificado) y no devolver ningún dato de imagen en respuesta a una solicitud `GET` condicional (que incluye un encabezado `If-Modified-Since` o `If-None-Match` válido).
