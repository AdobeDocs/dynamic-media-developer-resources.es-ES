---
description: Datos del mapa de imagen. Ninguno o más elementos HTML <AREA> completos, ordenados de frente a adelante.
seo-description: Datos del mapa de imagen. Ninguno o más elementos HTML <AREA> completos, ordenados de frente a adelante.
seo-title: Mapa
solution: Experience Manager
title: Mapa
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 5%

---


# Mapa{#map}

Datos del mapa de imagen. Ninguno o más elementos HTML `<AREA>` completos, ordenados de frente a atrás.

El servidor interpretará y puede cambiar los atributos SHAPE y COORDS. (SHAPE=CIRCLE no es compatible con esta versión). Todos los demás atributos de `<AREA>` se pasan sin modificación. Los valores de coordenadas especificados con el atributo COORDS deben ser desplazamientos de píxeles desde la esquina superior izquierda de la imagen de origen sin modificar. (`%` coordenadas no son compatibles con esta versión y pueden no procesarse correctamente).

## Propiedades {#section-f52d89fd399b4356ac05277e6c12f956}

Valor de cadena de texto. Si se especifica, debe ser uno o más elementos HTML `<AREA>` completos.

Este campo participa en la localización de cadenas de texto. Consulte [Localización de cadena de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en la *Referencia del protocolo HTTP* para obtener más información.

## Predeterminado {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Ninguno.

## Véase también {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ,  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), Localización de cadena  [de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
