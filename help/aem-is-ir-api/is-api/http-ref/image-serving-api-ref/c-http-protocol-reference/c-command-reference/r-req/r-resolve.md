---
description: Solicitud de depuración. Este comando de depuración analiza y preprocesa la solicitud, ejecuta búsquedas en el catálogo de imágenes, incluye modificadores de catálogo, sustituye macros y variables, etc., como req=img.
solution: Experience Manager
title: resolver
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 2%

---

# resolver{#resolve}

Solicitud de depuración. Este comando de depuración analiza y preprocesa la solicitud, ejecuta búsquedas en el catálogo de imágenes, inclusiones catalog::Modifier, sustituciones de macros y variables, etc., como req=img.

`req=resolve`

Se devuelve la cadena de solicitud final, en lugar de la imagen resultante, con tipo MIME `text/plain`.

La respuesta HTTP no se puede almacenar en caché.
