---
description: Datos de mapa de imagen. Ninguno o más HTML completos <area> elementos, ordenados de adelante hacia atrás.
solution: Experience Manager
title: Mapa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 4%

---

# Mapa{#map}

Datos de mapa de imagen. Ninguno o más HTML completos `<AREA>` elementos, ordenados de adelante hacia atrás.

El servidor interpreta y puede cambiar los atributos SHAPE y COORDS (SHAPE=CIRCLE no se admite en esta versión). Todos los demás atributos de `<AREA>` se pasan sin modificaciones. Los valores de coordenadas especificados con el atributo COORDS deben ser desplazamientos de píxeles desde la esquina superior izquierda de la imagen de origen sin modificar. (`%` las coordenadas no son compatibles con esta versión y es posible que no se procesen correctamente).

## Propiedades {#section-f52d89fd399b4356ac05277e6c12f956}

Valor de cadena de texto. Si se especifica, debe ser uno o más HTML completos `<AREA>` elementos.

Este campo participa en la localización de cadenas de texto. Consulte [Localización de cadenas de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en el *Referencia de protocolo HTTP* para obtener más información.

## Predeterminado {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Ninguno.

## Véase también {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localización de cadenas de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
