---
description: Algunas restricciones se aplican para anidar e incrustar.
solution: Experience Manager
title: Restricciones
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Restricciones{#restrictions}

Algunas restricciones se aplican para anidar e incrustar.

Para un buen rendimiento del servidor, la resolución de imágenes devueltas por las solicitudes anidadas debe coincidir razonablemente con la resolución de textura de los objetos a los que se aplica el material.

Las imágenes extranjeras se almacenan en caché localmente. Los cambios realizados en estas imágenes se detectarán solo después de que la entrada de caché local quede obsoleta (según el encabezado HTTP caducado).
