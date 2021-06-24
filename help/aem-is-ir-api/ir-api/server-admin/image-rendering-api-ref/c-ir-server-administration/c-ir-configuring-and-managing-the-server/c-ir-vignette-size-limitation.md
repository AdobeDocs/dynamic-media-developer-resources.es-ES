---
description: El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidales.
solution: Experience Manager
title: Limitación del tamaño de la viñeta
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# Limitación del tamaño de la viñeta{#vignette-size-limitation}

El procesamiento de imágenes impone una limitación de tamaño de dos Megapixels para las viñetas no piramidales.

Modifique el valor de `IrMaxNonPyrVignetteSize` en [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si su aplicación requiere soporte para viñetas que no sean piramidales con un área de imagen (anchura x altura) mayor que este límite.

>[!NOTE]
>
>`attribute::MaxPix` y también  `IS::MaxMessageSize` puede ser necesario ajustar para permitir tamaños de imagen de respuesta inusualmente grandes. Consulte la documentación de Image Serving para obtener más información.
