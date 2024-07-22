---
description: Tipo de recurso. Se utiliza para identificar el tipo de conjunto publicado en el conjunto de imágenes del catálogo.
solution: Experience Manager
title: AssetType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84530842-4d2a-402a-b94b-45356cec5dc1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# AssetType{#assettype}

Tipo de recurso. Se utiliza para identificar el tipo de conjunto publicado en catalog::ImageSet.

El tipo de recurso determina qué tipo de respuesta generar para `req=set` solicitudes. Si no se especifica un valor, las reglas de detección automática determinan el tipo de respuesta `req=set`.

## Propiedades {#properties}

Valor de enumeración del siguiente conjunto:

MEDIASET

SPINSET

SPINSET2D

VIDEOSET

IMAGESET

CATÁLOGO ELÉCTRICO

## Predeterminado {#section-b94ce61423194729918456103ef3f72c}

Ninguno.

## Véase también {#section-235f9f5522024d3682ee7cc0101eb7ba}

[catálogo::Conjunto de imágenes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [req=set](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Solicitudes de conjunto de medios](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md)
