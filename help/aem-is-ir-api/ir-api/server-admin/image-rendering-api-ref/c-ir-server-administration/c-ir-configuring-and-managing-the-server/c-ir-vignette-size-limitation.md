---
description: El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidales.
seo-description: El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidales.
seo-title: Limitación del tamaño de la viñeta
solution: Experience Manager
title: Limitación del tamaño de la viñeta
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Límite de tamaño de viñeta{#vignette-size-limitation}

El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidales.

Modifique el valor de `IrMaxNonPyrVignetteSize` en [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si su aplicación requiere soporte para viñetas que no sean piramidales con un área de imagen (anchura x altura) mayor que este límite.

>[!NOTE]
>
>`attribute::MaxPix` y también  `IS::MaxMessageSize` puede ser necesario ajustar para permitir tamaños de imagen de respuesta inusualmente grandes. Consulte la documentación de Image Serving para obtener más información.

