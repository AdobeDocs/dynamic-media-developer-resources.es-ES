---
description: Datos de mapa de imagen. Ninguno o más elementos <AREA> de HTML completos, ordenados de adelante hacia atrás.
solution: Experience Manager
title: Mapa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
TQID: 'https://experienceleague.adobe.com/JY0barcvbF72sTyYW4iIhjFE-8tfqtbI78PDccLcXV0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 4%

---

# Mapa{#map}

Datos de mapa de imagen. Ninguno o más elementos HTML `<AREA>` completos, ordenados de adelante hacia atrás.

El servidor interpreta y puede cambiar los atributos SHAPE y COORDS (SHAPE=CIRCLE no se admite en esta versión). Todos los demás atributos de `<AREA>` se pasan sin modificación. Los valores de coordenadas especificados con el atributo COORDS deben ser desplazamientos de píxeles desde la esquina superior izquierda de la imagen de origen sin modificar. (`%` coordenadas no son compatibles con esta versión y es posible que no se procesen correctamente).

## Propiedades {#section-f52d89fd399b4356ac05277e6c12f956}

Valor de cadena de texto. Si se especifica, debe ser uno o más elementos HTML `<AREA>` completos.

Este campo participa en la localización de cadenas de texto. Consulte [Localización de cadenas de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en la *Referencia de protocolo HTTP* para obtener detalles.

## Predeterminado {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Ninguno.

## Véase también {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localización de cadenas de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
