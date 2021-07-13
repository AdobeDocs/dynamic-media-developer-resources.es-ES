---
description: Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.
solution: Experience Manager
title: Uso de mapas de iluminación múltiple
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Uso de mapas de iluminación múltiple{#using-multiple-illumination-maps}

Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.

Se pueden crear hasta tres mapas de iluminación para cada viñeta. El mapa de iluminación de una operación de renderización se selecciona con los comandos `illum=` o `gloss=`.

**Selección** predeterminadaSi no se especifica  `illum=` ni  `gloss=` se especifica, el renderizador utilizará el primer mapa de iluminación creado (normalmente mapa A, también conocido como mapa de iluminación &quot;plana&quot;).

**Selección automática con`gloss=`** Si no  `illum=` se especifica o se establece en -1, el renderizador compara el  `gloss=` valor especificado con los valores de brillo asociados con cada mapa de iluminación de la viñeta y elige el mapa de iluminación cuyo valor de brillo sea más cercano al especificado  `gloss=`.

**Selección explícita con`illum=`** Si  `illum=` se especifica y se establece en 0, 1 o 2, el renderizador utilizará el mapa de iluminación correspondiente;  `gloss=` se ignora para seleccionar el mapa de iluminación.

Si la viñeta contiene solo un mapa de iluminación, el renderizador utilizará ese mapa e ignorará los comandos `illum=` y `gloss=`.
