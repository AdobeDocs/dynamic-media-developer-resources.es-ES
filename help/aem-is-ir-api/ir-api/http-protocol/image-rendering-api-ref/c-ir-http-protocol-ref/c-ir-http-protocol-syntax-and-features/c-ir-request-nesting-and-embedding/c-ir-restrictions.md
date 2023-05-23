---
title: Restricciones
description: Se aplican algunas restricciones para anidar e incrustar.
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

Se aplican algunas restricciones para anidar e incrustar.

Para obtener un buen rendimiento del servidor, la resolución de las imágenes devueltas por las solicitudes anidadas debe coincidir razonablemente con la resolución de textura de los objetos a los que se aplica el material.

Las imágenes externas se almacenan en caché localmente. Cualquier cambio en estas imágenes se detecta solo después de que la entrada de la caché local quede obsoleta (según el encabezado HTTP expires ).
