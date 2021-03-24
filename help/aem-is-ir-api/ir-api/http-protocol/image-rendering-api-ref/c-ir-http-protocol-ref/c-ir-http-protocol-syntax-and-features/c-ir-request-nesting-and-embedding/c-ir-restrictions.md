---
description: Algunas restricciones se aplican para anidar e incrustar.
solution: Experience Manager
title: Restricciones
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Restricciones{#restrictions}

Algunas restricciones se aplican para anidar e incrustar.

Para un buen rendimiento del servidor, la resolución de imágenes devueltas por las solicitudes anidadas debe coincidir razonablemente con la resolución de textura de los objetos a los que se aplica el material.

Las imágenes extranjeras se almacenan en caché localmente. Los cambios realizados en estas imágenes se detectarán solo después de que la entrada de caché local quede obsoleta (según el encabezado HTTP caducado).
