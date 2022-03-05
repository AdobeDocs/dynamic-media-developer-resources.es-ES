---
title: Uso de mapas de iluminación múltiple
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

# Uso de mapas de iluminación múltiple{#using-multiple-illumination-maps}

Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.

Se pueden crear hasta tres mapas de iluminación para cada viñeta. El mapa de iluminación de una operación de renderización se selecciona con la variable `illum=` y `gloss=` comandos.

**Selección predeterminada** - Si `illum=` o `gloss=` no se especifican, el renderizador utiliza el primer mapa de iluminación creado (normalmente mapa A, también conocido como mapa de iluminación &quot;plano&quot;).

**Selección automática con`gloss=`** - Si `illum=` no se ha especificado o está establecido en `-1`, el procesador compara el `gloss=` con los valores de brillo asociados a cada mapa de iluminación de la viñeta. Elige el mapa de iluminación cuyo valor de brillo sea más cercano al especificado `gloss=`.

**Selección explícita con`illum=`** - Si `illum=` se especifica y se establece como `0`, `1`o `2`, el renderizador utiliza el mapa de iluminación correspondiente; `gloss=` se ignora al seleccionar el mapa de iluminación.

Si la viñeta contiene solo un mapa de iluminación, el renderizador utiliza ese mapa e ignora el `illum=` y `gloss=` comandos.
