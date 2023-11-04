---
description: Ruta del archivo de máscara. Ruta de acceso relativa o absoluta y nombre para un archivo de imagen de máscara asociado a este registro de catálogo.
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# MaskPath{#maskpath}

Ruta del archivo de máscara. Ruta de acceso relativa o absoluta y nombre para un archivo de imagen de máscara asociado a este registro de catálogo.

Permite adjuntar máscaras independientes a las imágenes.

El servidor utiliza las reglas de resolución de rutas descritas en [Administración de datos de origen](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) para buscar el archivo de datos.

## Propiedades {#section-cdc3b7e2811e41008479cd97887c01b7}

Valor de cadena de texto. Opcional. Si se especifica, debe ser una ruta de archivo relativa o absoluta del servidor de imágenes válida. `attribute::DefaultExt` se anexa si no hay ningún sufijo de archivo.

Si una imagen principal ( `catalog::Path`) y una imagen de máscara ( `catalog::MaskPath`) se definen en un registro de catálogo, ambos deben tener exactamente el mismo tamaño de píxel. Las imágenes de máscara deben tener una escala de grises de 8 bits.

`mask=` en las anulaciones de solicitud `catalog::MaskPath`.

`catalog::MaskPath` reemplaza el canal alfa en la imagen principal ( `catalog::Path`), si está presente, y si el canal alfa no está asociado (es decir, no premultiplicado). Si la imagen alfa se multiplica previamente, `catalog::MaskPath` se ignora y siempre se utiliza el canal alfa.

## Predeterminado {#section-78533e35bfec469ba087cb68a35bb81b}

Ninguno.

## Véase también {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
