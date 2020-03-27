---
description: Imagen en miniatura. Solicita datos de imagen formateados y de tamaño mediante criterios de miniatura del catálogo.
seo-description: Imagen en miniatura. Solicita datos de imagen formateados y de tamaño mediante criterios de miniatura del catálogo.
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# tmb{#tmb}

Imagen en miniatura. Solicita datos de imagen formateados y de tamaño mediante criterios de miniatura del catálogo.

`req=tmb`

El formato de datos de respuesta y el tipo MIME de respuesta están determinados por `fmt=`. Admite todos los comandos excepto `fit=`.

Consulte Escalado [de miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.
