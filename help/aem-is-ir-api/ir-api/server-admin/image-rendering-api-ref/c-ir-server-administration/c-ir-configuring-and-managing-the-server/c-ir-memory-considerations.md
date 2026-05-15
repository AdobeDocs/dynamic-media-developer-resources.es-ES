---
description: La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas viñetas diferentes, el tamaño y la complejidad de las viñetas, etc.).
solution: Experience Manager
title: Consideraciones de memoria
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
TQID: 'https://experienceleague.adobe.com/l41dx4mMn82TvImVVCJJKgJZbP-mWT5KbnzfZ5xFJqg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 0%

---

# Consideraciones de memoria{#memory-considerations}

La cantidad de memoria utilizada por el procesamiento de imágenes puede variar ampliamente y depende en gran medida de la carga y el uso reales del servidor (por ejemplo, pocas viñetas frente a muchas viñetas diferentes, el tamaño y la complejidad de las viñetas, etc.).

Para obtener el mejor rendimiento, se debe evitar la paginación de memoria (intercambio).

Image Rendering comparte la administración de memoria del servidor de imágenes. Al utilizar el procesamiento de imágenes, se debe asignar memoria adicional. Entre el 30 y el 50% de la memoria física puede ser razonable.

Consulte la documentación del servicio de imágenes para obtener información sobre cómo cambiar la asignación de memoria del servidor de imágenes (ImageServer::PhysicalMemory).
