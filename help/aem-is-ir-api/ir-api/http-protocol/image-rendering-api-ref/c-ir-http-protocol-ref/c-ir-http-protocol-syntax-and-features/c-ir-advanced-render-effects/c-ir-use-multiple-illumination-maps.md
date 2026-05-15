---
title: Uso de mapas de iluminación múltiples
description: Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
TQID: 'https://experienceleague.adobe.com/VVZ1IdVJ85V-mIrdN6O8Vs-gb4PTsnjxyHnC8oEh1y0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 0%

---

# Uso de mapas de iluminación múltiples{#using-multiple-illumination-maps}

Algunas aplicaciones pueden requerir un mapa de iluminación diferente para diferentes tipos de materiales.

Se pueden crear hasta tres mapas de iluminación para cada viñeta. El mapa de iluminación para una operación de procesamiento se selecciona con los comandos `illum=` y/o `gloss=`.

**Selección predeterminada**: si no se especifican `illum=` o `gloss=`, el procesador utiliza el primer mapa de iluminación creado (normalmente, el mapa A, también conocido como mapa de iluminación &quot;plano&quot;).

**Selección automática con`gloss=`**: si `illum=` no se especifica o se establece en `-1`, el procesador compara el valor `gloss=` especificado con los valores de brillo asociados a cada mapa de iluminación en la viñeta. Elige el mapa de iluminación cuyo valor de brillo sea más cercano al `gloss=` especificado.

**Selección explícita con`illum=`**: si `illum=` se especifica y se establece en `0`, `1` o `2`, el procesador utilizará el mapa de iluminación correspondiente; se omitirá `gloss=` para seleccionar el mapa de iluminación.

Si la viñeta contiene un solo mapa de iluminación, el procesador utilizará ese mapa e ignorará los comandos `illum=` y `gloss=`.
