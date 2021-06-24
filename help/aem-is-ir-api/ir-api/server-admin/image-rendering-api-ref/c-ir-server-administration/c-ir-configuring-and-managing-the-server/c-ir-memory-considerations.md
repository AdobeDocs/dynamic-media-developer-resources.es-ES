---
description: La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas otras, tamaño y complejidad diferentes de las viñetas, etc.).
solution: Experience Manager
title: Consideraciones sobre la memoria
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Consideraciones sobre la memoria{#memory-considerations}

La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas otras, tamaño y complejidad diferentes de las viñetas, etc.).

Para obtener el mejor rendimiento, se debe evitar la paginación de memoria (intercambio).

Image Rendering comparte la gestión de memoria del Image Server. Al utilizar la renderización de imágenes, se debe asignar memoria adicional. 30 a 50% de la memoria física puede ser razonable.

Consulte la documentación de Image Serving para obtener información sobre cómo cambiar la asignación de memoria del Image Server (ImageServer::PhysicalMemory).
