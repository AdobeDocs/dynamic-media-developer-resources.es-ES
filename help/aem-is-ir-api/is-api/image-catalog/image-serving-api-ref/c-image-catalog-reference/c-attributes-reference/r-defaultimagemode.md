---
description: Modo de imagen predeterminado. Selecciona cómo se aplica la imagen predeterminada cuando no se encuentran las imágenes especificadas en la solicitud.
seo-description: Modo de imagen predeterminado. Selecciona cómo se aplica la imagen predeterminada cuando no se encuentran las imágenes especificadas en la solicitud.
seo-title: DefaultImageMode
solution: Experience Manager
title: DefaultImageMode
uuid: e5640f09-e1e3-473b-8fbc-84c6bfce2460
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# DefaultImageMode{#defaultimagemode}

Modo de imagen predeterminado. Selecciona cómo se aplica la imagen predeterminada cuando no se encuentran las imágenes especificadas en la solicitud.

## Propiedades {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. &#39;0&#39; para reemplazar toda la imagen compuesta, incluso si la imagen que falta es solo una de varias capas; &quot;1&quot; para reemplazar cada imagen de origen de capa que falta por la imagen predeterminada y devolver el compuesto como de costumbre.

## Restricciones {#section-04cb0d50e8914564a8d226d0d4663c8b}

El servicio de imágenes vuelve a `DefaultImageMode=0` cuando fallan las solicitudes anidadas de renderización de imágenes, FXG o `req=set`.

## Predeterminado {#section-9e318524a2a5496386901286748c7ee7}

Se hereda de `default::DefaultImage` si no está definido o si está vacío.

## Véase también {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
