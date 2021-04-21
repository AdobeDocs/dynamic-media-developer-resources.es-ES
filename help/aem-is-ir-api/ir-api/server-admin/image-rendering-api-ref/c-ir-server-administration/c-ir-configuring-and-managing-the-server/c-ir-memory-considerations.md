---
description: La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas otras, tamaño y complejidad diferentes de las viñetas, etc.).
solution: Experience Manager
title: Consideraciones sobre la memoria
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Consideraciones de memoria{#memory-considerations}

La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas otras, tamaño y complejidad diferentes de las viñetas, etc.).

Para obtener el mejor rendimiento, se debe evitar la paginación de memoria (intercambio).

Image Rendering comparte la gestión de memoria del Image Server. Al utilizar la renderización de imágenes, se debe asignar memoria adicional. 30 a 50% de la memoria física puede ser razonable.

Consulte la documentación de Image Serving para obtener información sobre cómo cambiar la asignación de memoria del Image Server (ImageServer::PhysicalMemory).
