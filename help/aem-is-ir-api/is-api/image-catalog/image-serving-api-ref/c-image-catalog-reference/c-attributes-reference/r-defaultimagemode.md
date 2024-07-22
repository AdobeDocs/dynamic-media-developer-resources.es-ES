---
description: Modo de imagen predeterminado. Selecciona cómo se aplica la imagen predeterminada cuando no se encuentran las imágenes especificadas en la solicitud.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# DefaultImageMode{#defaultimagemode}

Modo de imagen predeterminado. Selecciona cómo se aplica la imagen predeterminada cuando no se encuentran las imágenes especificadas en la solicitud.

## Propiedades {#section-7fa8acb63540490d9f5186231b5e77c3}

Enumeración. &#39;0&#39; para reemplazar toda la imagen compuesta, incluso si la imagen que falta es solo una de varias capas; &#39;1&#39; para reemplazar cada imagen de origen de capa que falte con la imagen predeterminada y devolver el compuesto de la forma habitual.

## Restricciones {#section-04cb0d50e8914564a8d226d0d4663c8b}

El servicio de imágenes vuelve a `DefaultImageMode=0` cuando las solicitudes de Image Rendering, FXG o `req=set` anidadas dan error.

## Predeterminado {#section-9e318524a2a5496386901286748c7ee7}

Se hereda de `default::DefaultImage` si no se ha definido o está vacío.

## Véase también {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) , [atributo::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
