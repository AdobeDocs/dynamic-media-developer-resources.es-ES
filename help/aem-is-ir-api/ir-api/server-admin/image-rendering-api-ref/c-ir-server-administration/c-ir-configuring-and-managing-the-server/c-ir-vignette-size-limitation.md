---
description: El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidables.
seo-description: El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidables.
seo-title: Limitación del tamaño de la viñeta
solution: Experience Manager
title: Limitación del tamaño de la viñeta
topic: Scene7 Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Limitación del tamaño de la viñeta{#vignette-size-limitation}

El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidables.

Modifique el valor de `IrMaxNonPyrVignetteSize` en [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si su aplicación requiere compatibilidad con viñetas no piramidables con un área de imagen (anchura x altura) mayor que este límite.

>[!NOTE]
>
>`attribute::MaxPix` y también `IS::MaxMessageSize` puede ser necesario ajustar para permitir tamaños de imagen de respuesta inusualmente grandes. Consulte la documentación del servicio de imágenes para obtener más información.

