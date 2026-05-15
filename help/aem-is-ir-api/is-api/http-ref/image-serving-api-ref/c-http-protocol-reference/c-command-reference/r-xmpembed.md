---
title: xmpEmbed
description: Incrustar metadatos de XMP. Especifica si los metadatos de XMP deben incluirse en la imagen de respuesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
TQID: 'https://experienceleague.adobe.com/2pISbWU-Y-4szY0jmZswDIxvBrPlJ1yZmQby0sZ1v-o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 2%

---

# xmpEmbed{#xmpembed}

Incrustar metadatos de XMP. Especifica si los metadatos de XMP deben incluirse en la imagen de respuesta.

`xmpEmbed=0|1`

>[!NOTE]
>
>Los datos de XMP se pasan de la imagen de origen a la imagen de respuesta sin realizar modificaciones. Esto puede hacer que se incrusten datos incorrectos en la imagen de respuesta.

## Propiedades {#section-27024c4272f44d9a8c264a0629193af2}

Atributo de solicitud. Se ignora si la imagen de origen no contiene datos de XMP. Solo se procesan los datos de XMP de la imagen de origen de `layer=0`. Se omiten los datos de XMP de otras imágenes de capa.

Se ignora si el formato de imagen de salida no admite la incrustación de XMP. Consulte la descripción de `fmt=` para obtener una lista de los formatos de imagen de salida que admiten la incrustación de XMP.

## Predeterminado {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, para no incrustar rutas en imágenes de salida.

## Véase también {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
