---
description: Máscara de imagen. Solicita los datos de la máscara (canal alfa).
seo-description: Máscara de imagen. Solicita los datos de la máscara (canal alfa).
seo-title: máscara
solution: Experience Manager
title: máscara
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# mask{#mask}

Máscara de imagen. Solicita los datos de la máscara (canal alfa).

`req=mask`

Admite los mismos comandos que `req=img` y el servidor los procesa del mismo modo, pero en lugar de devolver los datos RGB o RGBA, el servidor descarta la información de color y devuelve únicamente los datos de máscara (canal alfa). El formato de datos de respuesta y el tipo MIME de respuesta están determinados por `fmt=`.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.
