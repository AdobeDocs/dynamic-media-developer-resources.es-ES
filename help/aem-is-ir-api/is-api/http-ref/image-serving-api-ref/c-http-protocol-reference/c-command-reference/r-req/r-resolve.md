---
description: Solicitud de depuración. Este comando de depuración analiza y preprocesa la solicitud, ejecuta búsquedas de catálogo de imágenes, inclusiones de Modificador de catálogo, sustituciones de variables y macros, etc., como req=img.
solution: Experience Manager
title: resolver
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 2%

---

# resolver{#resolve}

Solicitud de depuración. Este comando de depuración analiza y preprocesa la solicitud, ejecuta búsquedas de catálogo de imágenes, catálogo::inclusiones de Modificador, sustituciones de variables y macros, etc., como req=img.

`req=resolve`

Se devuelve la cadena de solicitud final, en lugar de la imagen de resultado, con el tipo MIME `text/plain`.

La respuesta HTTP no se puede almacenar en caché.
