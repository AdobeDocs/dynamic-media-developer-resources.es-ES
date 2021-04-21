---
description: Los datos de imagen se devuelven si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req= tiene uno de los siguientes valores img, debug.
solution: Experience Manager
title: Imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 1%

---


# Imágenes{#images}

Los datos de imagen se devuelven si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req= tiene uno de los siguientes valores: img, depurar

El tipo MIME de respuesta HTTP está determinado por `fmt=` o, si `fmt=` no se especifica, depende del valor de `attribute::Format`.

El estado de la respuesta HTTP es &#39;200 OK&#39; si el método de solicitud es incondicional `GET` o `HEAD`.

El servidor puede responder con el estado &quot;304&quot; (no modificado) y no devolver ningún dato de imagen en respuesta a una solicitud condicional `GET` (con el campo [!DNL If-Modified-Since] presente en el `request-header`).
