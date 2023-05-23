---
description: Tamaño de imagen. Tamaño en píxeles de la imagen de resolución completa a la que hace referencia la ruta del catálogo.
solution: Experience Manager
title: Tamaño
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 9%

---

# Tamaño{#size}

Tamaño de imagen. Tamaño en píxeles de la imagen de resolución completa a la que hace referencia catalog::Path.

Si se proporciona este valor, el servicio de imágenes lo utiliza para evitar tener que abrir la imagen para obtener el tamaño real de la misma.

>[!NOTE]
>
>If `catalog::Size`se proporciona y no es el mismo que el tamaño real de la imagen con resolución completa, lo que puede dar lugar a un comportamiento indefinido.

## Propiedades {#section-5c914ec8b1444a8e99d811b647cd42a3}

Dos números enteros, cada bueno que 0, separados por una coma. Opcional.

## Predeterminado {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Si el campo no está presente o si el campo está vacío, se utiliza el tamaño real de la imagen.

## Véase también {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
