---
description: Ruta del archivo de máscara. Ruta relativa o absoluta y nombre de un archivo de imagen de máscara asociado con este registro de catálogo.
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# MaskPath{#maskpath}

Ruta del archivo de máscara. Ruta relativa o absoluta y nombre de un archivo de imagen de máscara asociado con este registro de catálogo.

Permite adjuntar máscaras independientes a las imágenes.

El servidor utiliza las reglas de resolución de rutas descritas en [Administración de datos de origen](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) para encontrar el archivo de datos.

## Propiedades {#section-cdc3b7e2811e41008479cd97887c01b7}

Valor de cadena de texto. Opcional. Si se especifica, debe ser una ruta de archivo válida relativa o absoluta del servidor de imágenes. `attribute::DefaultExt` se anexa si no hay ningún sufijo de archivo presente.

Si tanto una imagen principal ( `catalog::Path`) como una imagen de máscara ( `catalog::MaskPath`) están definidas en un registro de catálogo, ambas deben tener exactamente el mismo tamaño de píxel. Las imágenes de máscara deben tener una escala de grises de 8 bits.

`mask=` en las anulaciones de solicitud  `catalog::MaskPath`.

`catalog::MaskPath` anula el canal alfa en la imagen principal (  `catalog::Path`), si está presente, y si el canal alfa no está asociado (es decir, no está premultiplicado). Si la imagen alfa está premultiplicada, `catalog::MaskPath` se ignora y siempre se utiliza el canal alfa.

## Predeterminado {#section-78533e35bfec469ba087cb68a35bb81b}

Ninguno.

## Véase también {#section-68d262f5949c4959b8723ba44611d1dc}

[atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [atributo::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md),  [catálogo::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c),  [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md),  [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
