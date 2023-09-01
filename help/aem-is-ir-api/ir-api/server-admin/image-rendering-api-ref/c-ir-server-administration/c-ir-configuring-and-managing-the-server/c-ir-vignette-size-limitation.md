---
title: Limitación de tamaño de viñeta
description: El procesamiento de imágenes impone una limitación de tamaño de dos megapíxeles para las viñetas que no son piramidales.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# Limitación de tamaño de viñeta{#vignette-size-limitation}

El procesamiento de imágenes impone una limitación de tamaño de dos megapíxeles para las viñetas que no son piramidales.

Modifique el valor de `IrMaxNonPyrVignetteSize` en [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si su aplicación requiere compatibilidad con viñetas que no sean piramidales con un área de imagen (anchura x altura) mayor que este límite.

>[!NOTE]
>
>Ajuste de los atributos `attribute::MaxPix` y `IS::MaxMessageSize` para permitir tamaños de imagen de respuesta inusualmente grandes. Consulte la documentación del servicio de imágenes para obtener más información.
