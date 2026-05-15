---
title: Limitación de tamaño de viñeta
description: El procesamiento de imágenes impone una limitación de tamaño de dos megapíxeles para las viñetas que no son piramidales.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
TQID: 'https://experienceleague.adobe.com/qPrnkvYXinvZAfx-s6ePjpe64qsoBfwtVbUJ-fYBbmc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 0%

---

# Limitación de tamaño de viñeta{#vignette-size-limitation}

El procesamiento de imágenes impone una limitación de tamaño de dos megapíxeles para las viñetas que no son piramidales.

Modifique el valor de `IrMaxNonPyrVignetteSize` en [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si su aplicación requiere compatibilidad con viñetas que no sean piramidales con un área de imagen (anchura x altura) mayor que este límite.

>[!NOTE]
>
>Ajuste los atributos `attribute::MaxPix` y `IS::MaxMessageSize` para permitir tamaños de imagen de respuesta inusualmente grandes. Consulte la documentación del servicio de imágenes para obtener más información.
