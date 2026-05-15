---
description: Ruta del archivo de máscara. Ruta de acceso relativa o absoluta y nombre para un archivo de imagen de máscara asociado a este registro de catálogo.
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
TQID: 'https://experienceleague.adobe.com/tUXD-vnkr3qkaH3B-dE-e9wfSPXAcnwRbqG9KuJej9E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 2%

---

# MaskPath{#maskpath}

Ruta del archivo de máscara. Ruta de acceso relativa o absoluta y nombre para un archivo de imagen de máscara asociado a este registro de catálogo.

Permite adjuntar máscaras independientes a las imágenes.

El servidor usa las reglas de resolución de rutas descritas en [Administrar datos de Source](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) para encontrar el archivo de datos.

## Propiedades {#section-cdc3b7e2811e41008479cd97887c01b7}

Valor de cadena de texto. Opcional. Si se especifica, debe ser una ruta de archivo relativa o absoluta del servidor de imágenes válida. `attribute::DefaultExt` se anexa si no hay ningún sufijo de archivo.

Si una imagen principal (`catalog::Path`) y una imagen de máscara (`catalog::MaskPath`) están definidas en un registro de catálogo, ambas deben tener exactamente el mismo tamaño de píxel. Las imágenes de máscara deben tener una escala de grises de 8 bits.

`mask=` en la solicitud invalida `catalog::MaskPath`.

`catalog::MaskPath` reemplaza el canal alfa en la imagen principal ( `catalog::Path`), si está presente, y si el canal alfa no está asociado (es decir, no premultiplicado). Si la imagen alfa se multiplica previamente, `catalog::MaskPath` se omitirá y el canal alfa se utilizará siempre.

## Predeterminado {#section-78533e35bfec469ba087cb68a35bb81b}

Ninguno.

## Véase también {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catálogo::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [máscara=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=máscara](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
