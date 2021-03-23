---
description: Imagen en miniatura. Solicita datos de imagen con formato y tamaño utilizando criterios de vista en miniatura del catálogo.
seo-description: Imagen en miniatura. Solicita datos de imagen con formato y tamaño utilizando criterios de vista en miniatura del catálogo.
seo-title: tmb
solution: Experience Manager
title: tmb
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# tmb{#tmb}

Imagen en miniatura. Solicita datos de imagen con formato y tamaño utilizando criterios de vista en miniatura del catálogo.

`req=tmb`

El formato de datos de respuesta y el tipo MIME de respuesta están determinados por `fmt=`. Admite todos los comandos excepto `fit=`.

Consulte [Escalado de miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.
