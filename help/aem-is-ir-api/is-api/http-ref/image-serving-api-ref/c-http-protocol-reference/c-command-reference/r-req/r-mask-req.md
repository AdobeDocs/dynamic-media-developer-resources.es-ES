---
description: Máscara de imagen. Solicita los datos de la máscara (canal alfa).
seo-description: Máscara de imagen. Solicita los datos de la máscara (canal alfa).
seo-title: mask
solution: Experience Manager
title: mask
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# mask{#mask}

Máscara de imagen. Solicita los datos de la máscara (canal alfa).

`req=mask`

Admite los mismos comandos que `req=img` y el servidor los procesa del mismo modo, pero en lugar de devolver los datos RGB o RGBA, el servidor descarta la información de color y devuelve únicamente los datos de máscara (canal alfa). El formato de datos de respuesta y el tipo MIME de respuesta están determinados por `fmt=`.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.
