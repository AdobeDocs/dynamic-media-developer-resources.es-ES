---
description: La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas viñetas diferentes, el tamaño y la complejidad de las viñetas, etc.).
solution: Experience Manager
title: Consideraciones de memoria
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Consideraciones de memoria{#memory-considerations}

La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas viñetas diferentes, el tamaño y la complejidad de las viñetas, etc.).

Para obtener el mejor rendimiento, se debe evitar la paginación de memoria (intercambio).

Image Rendering comparte la administración de memoria del servidor de imágenes. Al utilizar el procesamiento de imágenes, se debe asignar memoria adicional. Entre el 30 y el 50% de la memoria física puede ser razonable.

Consulte la documentación del servicio de imágenes para obtener información sobre cómo cambiar la asignación de memoria del servidor de imágenes (ImageServer::PhysicalMemory).
