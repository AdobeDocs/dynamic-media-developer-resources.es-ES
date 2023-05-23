---
description: El procesamiento de imágenes impone una limitación de tamaño de dos megapíxeles para las viñetas que no son piramidales.
solution: Experience Manager
title: Limitación de tamaño de viñeta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# Limitación de tamaño de viñeta{#vignette-size-limitation}

El procesamiento de imágenes impone una limitación de tamaño de dos megapíxeles para las viñetas que no son piramidales.

Modifique el valor de `IrMaxNonPyrVignetteSize` en [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si su aplicación requiere compatibilidad con viñetas que no sean piramidales con un área de imagen (anchura x altura) mayor que este límite.

>[!NOTE]
>
>`attribute::MaxPix` y `IS::MaxMessageSize` también puede ser necesario ajustar para permitir tamaños de imagen de respuesta inusualmente grandes. Consulte la documentación del servicio de imágenes para obtener más información.
