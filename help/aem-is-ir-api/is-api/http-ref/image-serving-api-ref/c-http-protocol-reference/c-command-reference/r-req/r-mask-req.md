---
description: Máscara de imagen. Solicita los datos de la máscara (canal alfa).
seo-description: Máscara de imagen. Solicita los datos de la máscara (canal alfa).
seo-title: máscara
solution: Experience Manager
title: máscara
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mask{#mask}

Máscara de imagen. Solicita los datos de la máscara (canal alfa).

`req=mask`

Admite los mismos comandos que `req=img`y el servidor los procesa de la misma manera, pero en lugar de devolver los datos RGB o RGBA, el servidor descarta la información de color y devuelve sólo los datos de máscara (canal alfa). El formato de datos de respuesta y el tipo MIME de respuesta están determinados por `fmt=`.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.
