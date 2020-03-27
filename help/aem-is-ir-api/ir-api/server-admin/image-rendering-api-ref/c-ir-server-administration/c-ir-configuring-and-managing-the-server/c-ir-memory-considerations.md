---
description: La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas o muchas viñetas diferentes, tamaño y complejidad de las viñetas, etc.).
seo-description: La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas o muchas viñetas diferentes, tamaño y complejidad de las viñetas, etc.).
seo-title: Consideraciones sobre la memoria
solution: Experience Manager
title: Consideraciones sobre la memoria
topic: Scene7 Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Consideraciones sobre la memoria{#memory-considerations}

La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas o muchas viñetas diferentes, tamaño y complejidad de las viñetas, etc.).

Para un mejor rendimiento, se debe evitar la paginación de memoria (intercambio).

El procesamiento de imágenes comparte la administración de memoria del servidor de imágenes. Al utilizar el procesamiento de imágenes, se debe asignar memoria adicional. 30 a 50% de la memoria física puede ser razonable.

Consulte la documentación del servicio de imágenes para obtener información sobre cómo cambiar la asignación de memoria del servidor de imágenes (ImageServer::PhysicalMemory).
