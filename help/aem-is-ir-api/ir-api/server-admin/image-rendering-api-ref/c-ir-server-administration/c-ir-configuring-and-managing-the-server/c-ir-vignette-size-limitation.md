---
description: El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidables.
seo-description: El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidables.
seo-title: Limitación del tamaño de la viñeta
solution: Experience Manager
title: Limitación del tamaño de la viñeta
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Límite de tamaño de viñeta{#vignette-size-limitation}

El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidables.

Modifique el valor de `IrMaxNonPyrVignetteSize` en [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si su aplicación requiere compatibilidad con viñetas no piramidables con un área de imagen (anchura x altura) mayor que este límite.

>[!NOTE]
>
>`attribute::MaxPix` y también  `IS::MaxMessageSize` puede ser necesario ajustar para permitir tamaños de imagen de respuesta inusualmente grandes. Consulte la documentación del servicio de imágenes para obtener más información.

