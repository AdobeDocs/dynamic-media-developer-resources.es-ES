---
description: Los datos de imagen se devuelven si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req=img o req=tmb.
seo-description: Los datos de imagen se devuelven si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req=img o req=tmb.
seo-title: Imágenes
solution: Experience Manager
title: Imágenes
topic: Scene7 Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# Imágenes{#images}

Los datos de imagen se devuelven si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req=img o req=tmb.

El tipo MIME de respuesta HTTP está determinado por `fmt=` o, si no se especifica `fmt=`, es `<image/jpeg>`.

El estado de la respuesta HTTP es &#39;200 OK&#39; si el método de solicitud era un `GET` o `HEAD` incondicional.

El servidor puede responder con el estado &#39;304&#39; (no modificado) y no devolver ningún dato de imagen en respuesta a una solicitud condicional `GET` (que incluye un encabezado `If-Modified-Since` o `If-None-Match` válido).
