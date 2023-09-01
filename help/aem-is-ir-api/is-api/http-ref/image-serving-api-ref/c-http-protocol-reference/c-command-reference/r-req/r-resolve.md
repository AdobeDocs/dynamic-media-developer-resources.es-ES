---
title: resolver
description: Solicitud de depuración. Este comando de depuración analiza y preprocesa la solicitud, ejecuta búsquedas en el catálogo de imágenes, inclusiones de modificadores de catálogo, sustituciones de variables y macros, etc., como req=img.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# resolver{#resolve}

Solicitud de depuración. Este comando de depuración analiza y preprocesa la solicitud, ejecuta búsquedas en el catálogo de imágenes, inclusiones catalog::Modifier, sustituciones de macros y variables, etc., como req=img.

`req=resolve`

Se devuelve la cadena de solicitud final, en lugar de la imagen resultante, con tipo MIME `text/plain`.

La respuesta HTTP no se puede almacenar en caché.
