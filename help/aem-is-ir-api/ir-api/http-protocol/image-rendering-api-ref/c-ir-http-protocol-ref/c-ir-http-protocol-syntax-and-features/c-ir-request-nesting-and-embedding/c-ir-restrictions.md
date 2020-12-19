---
description: Algunas restricciones se aplican para anidar e incrustar.
seo-description: Algunas restricciones se aplican para anidar e incrustar.
seo-title: Restricciones
solution: Experience Manager
title: Restricciones
topic: Scene7 Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Restricciones{#restrictions}

Algunas restricciones se aplican para anidar e incrustar.

Para un buen rendimiento del servidor, la resolución de las imágenes devueltas por las solicitudes anidadas debe coincidir razonablemente con la resolución de textura de los objetos a los que se está aplicando el material.

Las imágenes extranjeras se almacenan en caché localmente. Cualquier cambio en estas imágenes se detectará solamente después de que la entrada de caché local se haya quedado obsoleta (según el encabezado HTTP caduca).
