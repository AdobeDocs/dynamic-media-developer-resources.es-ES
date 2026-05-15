---
title: Imágenes
description: Se devuelven datos de imagen si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req= tiene uno de los siguientes valores img, debug.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
TQID: 'https://experienceleague.adobe.com/4wHyyXX0gxz9ojr5g5Puu5fBhKXo4hZDjyBuVTao3rQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 1%

---

# Imágenes{#images}

Se devuelven datos de imagen si una solicitud se completa correctamente y si la solicitud no incluye un comando req= o si req= tiene uno de los siguientes valores: img, debug

El tipo MIME de respuesta HTTP está determinado por `fmt=` o, si no se especifica `fmt=`, depende del valor de `attribute::Format`.

El estado de la respuesta HTTP es &#39;200 OK&#39; si el método de solicitud era un `GET` o `HEAD` incondicional.

El servidor puede responder con el estado &quot;304&quot; (no modificado) y no devolver ningún dato de imagen en respuesta a una solicitud `GET` condicional (con el campo [!DNL If-Modified-Since] presente en `request-header`).
