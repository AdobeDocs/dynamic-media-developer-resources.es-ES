---
description: Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.
seo-description: Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.
seo-title: Uso de mapas de iluminación múltiple
solution: Experience Manager
title: Uso de mapas de iluminación múltiple
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Uso de mapas de iluminación múltiple{#using-multiple-illumination-maps}

Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.

Se pueden crear hasta tres mapas de iluminación para cada viñeta. El mapa de iluminación de una operación de renderización se selecciona con los comandos `illum=` o `gloss=`.

**Selección** predeterminadaSi no se especifica  `illum=` ni  `gloss=` se especifica, el renderizador utilizará el primer mapa de iluminación creado (normalmente mapa A, también conocido como mapa de iluminación &quot;plana&quot;).

**Selección automática con`gloss=`** Si no  `illum=` se especifica o se establece en -1, el renderizador compara el  `gloss=` valor especificado con los valores de brillo asociados con cada mapa de iluminación de la viñeta y elige el mapa de iluminación cuyo valor de brillo sea más cercano al especificado  `gloss=`.

**Selección explícita con`illum=`** Si  `illum=` se especifica y se establece en 0, 1 o 2, el renderizador utilizará el mapa de iluminación correspondiente;  `gloss=` se ignora para seleccionar el mapa de iluminación.

Si la viñeta contiene solo un mapa de iluminación, el renderizador utilizará ese mapa e ignorará los comandos `illum=` y `gloss=`.
