---
title: Illum
description: Selector de mapa de iluminación. Permite la selección explícita del mapa de iluminación que se utilizará al procesar este material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e74b3e8-6289-4114-aa11-a6f91671363e
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 3%

---

# Illum{#illum}

Selector de mapa de iluminación. Permite la selección explícita del mapa de iluminación que se utilizará al procesar este material.

## Propiedades {#section-162bcf562ca844ccba9e81e267508cca}

Enumeración. Establezca el valor en -1 para la selección automática del mapa de iluminación en función del valor de catalog::Gloss.

Ajuste en 0, 1 o 2 para seleccionar el mapa de iluminación A, B o C. El procesador elige el mapa de iluminación más cercano disponible en la viñeta.

## Predeterminado {#section-ac386d31ef90423b8a367010a60bddc7}

-1 (selección automática)

## Véase también {#section-d9db8507a5e54692b84f54b3f84b782a}

[attribute::Brillo](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)
