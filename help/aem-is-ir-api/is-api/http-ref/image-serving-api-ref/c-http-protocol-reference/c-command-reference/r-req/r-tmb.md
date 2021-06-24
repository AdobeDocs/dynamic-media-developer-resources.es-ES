---
description: Imagen en miniatura. Solicita datos de imagen con formato y tamaño utilizando criterios de vista en miniatura del catálogo.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# tmb{#tmb}

Imagen en miniatura. Solicita datos de imagen con formato y tamaño utilizando criterios de vista en miniatura del catálogo.

`req=tmb`

El formato de datos de respuesta y el tipo MIME de respuesta están determinados por `fmt=`. Admite todos los comandos excepto `fit=`.

Consulte [Escalado de miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.
