---
description: Máscara de imagen. Solicita los datos de la máscara (canal alfa).
solution: Experience Manager
title: mask
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# mask{#mask}

Máscara de imagen. Solicita los datos de la máscara (canal alfa).

`req=mask`

Admite los mismos comandos que `req=img`. El servidor lo procesa del mismo modo, pero en lugar de devolver los datos RGB o RGBA, el servidor descarta la información de color y solo devuelve los datos de máscara (canal alfa). El formato de datos de respuesta y el tipo MIME de respuesta están determinados por `fmt=`.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.
