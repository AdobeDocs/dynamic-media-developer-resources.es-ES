---
description: Algunas restricciones se aplican para anidar e incrustar.
seo-description: Algunas restricciones se aplican para anidar e incrustar.
seo-title: Restricciones
solution: Experience Manager
title: Restricciones
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Restricciones{#restrictions}

Algunas restricciones se aplican para anidar e incrustar.

Para un buen rendimiento del servidor, la resolución de imágenes devueltas por las solicitudes anidadas debe coincidir razonablemente con la resolución de textura de los objetos a los que se aplica el material.

Las imágenes extranjeras se almacenan en caché localmente. Los cambios realizados en estas imágenes se detectarán solo después de que la entrada de caché local quede obsoleta (según el encabezado HTTP caducado).
