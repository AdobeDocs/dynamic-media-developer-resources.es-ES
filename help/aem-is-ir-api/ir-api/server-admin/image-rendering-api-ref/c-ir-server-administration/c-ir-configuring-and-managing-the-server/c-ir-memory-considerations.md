---
description: La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas otras, tamaño y complejidad diferentes de las viñetas, etc.).
seo-description: La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas otras, tamaño y complejidad diferentes de las viñetas, etc.).
seo-title: Consideraciones sobre la memoria
solution: Experience Manager
title: Consideraciones sobre la memoria
uuid: 21247081-ff27-4237-93da-5fc996417dfd
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Consideraciones de memoria{#memory-considerations}

La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas otras, tamaño y complejidad diferentes de las viñetas, etc.).

Para obtener el mejor rendimiento, se debe evitar la paginación de memoria (intercambio).

Image Rendering comparte la gestión de memoria del Image Server. Al utilizar la renderización de imágenes, se debe asignar memoria adicional. 30 a 50% de la memoria física puede ser razonable.

Consulte la documentación de Image Serving para obtener información sobre cómo cambiar la asignación de memoria del Image Server (ImageServer::PhysicalMemory).
