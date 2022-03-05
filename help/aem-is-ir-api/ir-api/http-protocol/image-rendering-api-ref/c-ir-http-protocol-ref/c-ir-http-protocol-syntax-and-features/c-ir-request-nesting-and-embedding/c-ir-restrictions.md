---
title: Restricciones
description: Algunas restricciones se aplican para anidar e incrustar.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Restricciones{#restrictions}

Algunas restricciones se aplican para anidar e incrustar.

Para un buen rendimiento del servidor, la resolución de las imágenes devueltas por las solicitudes anidadas debe coincidir razonablemente con la resolución de textura de los objetos a los que se aplica el material.

Las imágenes extranjeras se almacenan en caché localmente. Los cambios realizados en estas imágenes solo se detectan después de que la entrada de caché local se quede obsoleta (según el encabezado HTTP caducado).
