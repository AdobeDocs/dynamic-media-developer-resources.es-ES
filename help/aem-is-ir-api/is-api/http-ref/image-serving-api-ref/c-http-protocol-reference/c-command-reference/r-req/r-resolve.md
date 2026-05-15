---
title: resolver
description: Solicitud de depuración. Este comando de depuración analiza y preprocesa la solicitud, ejecuta búsquedas en el catálogo de imágenes, inclusiones de modificadores de catálogo, sustituciones de variables y macros, etc., como req=img.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
TQID: 'https://experienceleague.adobe.com/yS8k6Njz17UK9W42N6wyqmeg3FDweKnZ3vkMNw9wnJI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 2%

---

# resolver{#resolve}

Solicitud de depuración. Este comando de depuración analiza y preprocesa la solicitud, ejecuta búsquedas en el catálogo de imágenes, inclusiones catalog::Modifier, sustituciones de macros y variables, etc., como req=img.

`req=resolve`

Se devuelve la cadena de solicitud final, en lugar de la imagen resultante, con el tipo MIME `text/plain`.

La respuesta HTTP no se puede almacenar en caché.
