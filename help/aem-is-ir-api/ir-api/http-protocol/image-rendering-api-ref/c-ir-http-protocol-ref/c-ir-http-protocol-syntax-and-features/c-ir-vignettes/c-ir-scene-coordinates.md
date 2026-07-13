---
title: Coordenadas de escena
description: El espacio de coordenadas de escena se utiliza para especificar tamaños y distancias en las superficies de objeto texturables.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
TQID: 'https://experienceleague.adobe.com/eiZh-q74Q7fGwtuyj8dKSi8h-RMSjOSP7I6Wbq5FxTU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 0%

---

# Coordenadas de escena{#scene-coordinates}

El espacio de coordenadas de escena se utiliza para especificar tamaños y distancias en las superficies de objeto texturables.

Dado que la mayoría de las viñetas son escenas del mundo real que representan objetos físicos, la mayoría de las viñetas se crean utilizando pulgadas como unidades para el espacio de coordenadas de la escena. También pueden utilizarse otras unidades, como mm o cm. El procesamiento de imágenes no admite la conversión de unidades.

Los siguientes comandos aceptan valores en el espacio de coordenadas de la escena:

* [agrupar=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [size=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)

