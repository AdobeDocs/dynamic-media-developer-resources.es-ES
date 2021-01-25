---
description: Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.
seo-description: Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.
seo-title: Uso de mapas de iluminación múltiple
solution: Experience Manager
title: Uso de mapas de iluminación múltiple
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# Uso de mapas de iluminación múltiple{#using-multiple-illumination-maps}

Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.

Se pueden crear hasta tres mapas de iluminación para cada viñeta. El mapa de iluminación para una operación de procesamiento se selecciona con los comandos `illum=` y `gloss=`.

**Selección** predeterminadaSi no se especifica ninguno  `illum=` ni  `gloss=` se especifica ninguno, el procesador utilizará el primer mapa de iluminación creado (normalmente el mapa de iluminación A, denominado &quot;plano&quot;).

**Selección automática con`gloss=`** Si no  `illum=` se especifica o se establece en -1, el procesador compara el  `gloss=` valor especificado con los valores de brillo asociados a cada mapa de iluminación de la viñeta y elige el mapa de iluminación cuyo valor de brillo sea más cercano al especificado  `gloss=`.

**Selección explícita con`illum=`** Si  `illum=` se especifica y se establece en 0, 1 o 2, el procesador utilizará el mapa de iluminación correspondiente;  `gloss=` se ignora para seleccionar el mapa de iluminación.

Si la viñeta contiene sólo un mapa de iluminación, el procesador utilizará ese mapa e ignorará los comandos `illum=` y `gloss=`.
