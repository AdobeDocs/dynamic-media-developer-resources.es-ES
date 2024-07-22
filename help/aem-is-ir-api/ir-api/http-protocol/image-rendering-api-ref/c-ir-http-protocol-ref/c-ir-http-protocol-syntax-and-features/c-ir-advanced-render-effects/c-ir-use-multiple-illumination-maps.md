---
title: Uso de mapas de iluminación múltiples
description: Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Uso de mapas de iluminación múltiples{#using-multiple-illumination-maps}

Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.

Se pueden crear hasta tres mapas de iluminación para cada viñeta. El mapa de iluminación para una operación de procesamiento se selecciona con los comandos `illum=` y/o `gloss=`.

**Selección predeterminada**: si no se especifican `illum=` o `gloss=`, el procesador utiliza el primer mapa de iluminación creado (normalmente, el mapa A, también conocido como mapa de iluminación &quot;plano&quot;).

**Selección automática con`gloss=`**: si `illum=` no se especifica o se establece en `-1`, el procesador compara el valor `gloss=` especificado con los valores de brillo asociados a cada mapa de iluminación en la viñeta. Elige el mapa de iluminación cuyo valor de brillo sea más cercano al `gloss=` especificado.

**Selección explícita con`illum=`**: si `illum=` se especifica y se establece en `0`, `1` o `2`, el procesador utilizará el mapa de iluminación correspondiente; se omitirá `gloss=` para seleccionar el mapa de iluminación.

Si la viñeta contiene un solo mapa de iluminación, el procesador utilizará ese mapa e ignorará los comandos `illum=` y `gloss=`.
