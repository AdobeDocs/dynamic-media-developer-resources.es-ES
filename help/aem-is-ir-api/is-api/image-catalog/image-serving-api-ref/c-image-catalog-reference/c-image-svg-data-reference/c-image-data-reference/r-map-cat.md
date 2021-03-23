---
description: Datos del mapa de imágenes. Ninguno o más elementos HTML <AREA> completos, ordenados de frente a atrás.
seo-description: Datos del mapa de imágenes. Ninguno o más elementos HTML <AREA> completos, ordenados de frente a atrás.
seo-title: Mapa
solution: Experience Manager
title: Mapa
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 5%

---


# Mapa{#map}

Datos del mapa de imágenes. Ninguno o más elementos HTML `<AREA>` completos, ordenados de frente a atrás.

El servidor interpretará y puede cambiar los atributos SHAPE y COORDS. (SHAPE=CIRCLE no es compatible con esta versión). Todos los demás atributos de `<AREA>` se pasan sin modificación. Los valores de coordenadas especificados con el atributo COORDS deben ser desplazamientos de píxeles desde la esquina superior izquierda de la imagen de origen sin modificar. (`%` las coordenadas no son compatibles con esta versión y es posible que no se procesen correctamente).

## Propiedades {#section-f52d89fd399b4356ac05277e6c12f956}

Valor de cadena de texto. Si se especifica, debe ser uno o más elementos HTML `<AREA>` completos.

Este campo participa en la localización de cadenas de texto. Consulte [Localización de cadena de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en *Referencia de protocolo HTTP* para obtener más información.

## Predeterminado {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Ninguno.

## Véase también {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ,  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md),  [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
