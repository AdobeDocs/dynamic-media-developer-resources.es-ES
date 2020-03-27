---
description: Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.
seo-description: Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.
seo-title: Uso de mapas de iluminación múltiple
solution: Experience Manager
title: Uso de mapas de iluminación múltiple
topic: Scene7 Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Uso de mapas de iluminación múltiple{#using-multiple-illumination-maps}

Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.

Se pueden crear hasta tres mapas de iluminación para cada viñeta. El mapa de iluminación de una operación de procesamiento se selecciona con los comandos `illum=` y o `gloss=` .

**Selección** predeterminada Si no se especifica ni `illum=` ni `gloss=` , el procesador utilizará el primer mapa de iluminación creado (generalmente el mapa A, denominado mapa de iluminación &#39;Flat&#39;).

**Selección automática con`gloss=`**Si`illum=`no se especifica o se define como -1, el procesador compara el valor especificado`gloss=`con los valores de brillo asociados a cada mapa de iluminación de la viñeta y elige el mapa de iluminación cuyo valor de brillo sea el más cercano al especificado`gloss=`.

**Selección explícita con`illum=`**Si`illum=`se especifica y se establece en 0, 1 o 2, el procesador utilizará el mapa de iluminación correspondiente;`gloss=`se ignora para seleccionar el mapa de iluminación.

Si la viñeta contiene sólo un mapa de iluminación, el procesador utilizará ese mapa e ignorará los comandos `illum=` y `gloss=` .
