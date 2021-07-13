---
description: Máscara de imagen. Solicita los datos de la máscara (canal alfa).
solution: Experience Manager
title: mask
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# mask{#mask}

Máscara de imagen. Solicita los datos de la máscara (canal alfa).

`req=mask`

Admite los mismos comandos que `req=img`. El servidor lo procesa del mismo modo, pero en lugar de devolver los datos RGB o RGBA, el servidor descarta la información de color y solo devuelve los datos de máscara (canal alfa). El formato de datos de respuesta y el tipo MIME de respuesta están determinados por `fmt=`.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.
