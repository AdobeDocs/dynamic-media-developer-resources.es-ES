---
title: Imágenes
description: Se devuelven datos de imagen si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req= tiene uno de los siguientes valores img, debug.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# Imágenes{#images}

Se devuelven datos de imagen si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req= tiene uno de los siguientes valores: img, debug

El tipo MIME de respuesta HTTP está determinado por `fmt=`, o, si `fmt=` no se ha especificado, depende del valor de `attribute::Format`.

El estado de respuesta HTTP es &quot;200 OK&quot; si el método de solicitud es incondicional `GET` o `HEAD`.

El servidor puede responder con el estado &quot;304&quot; (no modificado) y no devolver ningún dato de imagen en respuesta a un condicional `GET` solicitud (con el [!DNL If-Modified-Since] campo presente en la `request-header`).
