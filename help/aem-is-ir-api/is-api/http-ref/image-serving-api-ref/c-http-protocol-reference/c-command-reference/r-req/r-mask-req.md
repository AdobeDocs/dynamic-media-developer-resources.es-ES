---
description: Máscara de imagen. Solicita los datos de la máscara (canal alfa).
solution: Experience Manager
title: enmascarar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# enmascarar{#mask}

Máscara de imagen. Solicita los datos de la máscara (canal alfa).

`req=mask`

Admite los mismos comandos que `req=img`. El servidor la procesa del mismo modo, pero en lugar de devolver los datos del RGB o RGBA, descarta la información de color y devuelve únicamente los datos de la máscara (canal alfa). El formato de datos de respuesta y el tipo MIME de respuesta están determinados por `fmt=`.

La respuesta HTTP se puede almacenar en caché con el TTL en función de `catalog::Expiration`.
