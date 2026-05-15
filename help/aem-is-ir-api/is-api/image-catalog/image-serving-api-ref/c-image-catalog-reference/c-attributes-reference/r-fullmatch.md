---
description: Opción de coincidencia de catálogo.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
TQID: 'https://experienceleague.adobe.com/5eTvORUSVsXHReAaiVMGSizooDQ9Wq--dXrBo0c9C7c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 1%

---

# FullMatch{#fullmatch}

Opción de coincidencia de catálogo.

Se ha especificado una entrada de catálogo como un par `*`rootId`*/ *`imageId`*` en las solicitudes HTTP. Al analizar, se selecciona un catálogo si `*`rootId`*` coincide con el valor `attribute::RootId` del catálogo, y el registro de catálogo se identifica haciendo coincidir `*`imageId`*` con un valor `catalog::Id`. Si se encuentra un catálogo, pero no hay ninguna entrada de catálogo que coincida con `*`imageId`*`, el servidor puede hacer una de las dos cosas:

Si `attribute::FullMatch` no está establecido, el servidor usa los atributos del catálogo coincidente. En este caso, `*`rootId`*` se reemplaza por `attribute::RootPath` (o `default::RootPath`, si no se especifica en este catálogo).

Si se establece `attribute::FullMatch`, el servidor ignora por completo el catálogo, como si no se hubiera encontrado ningún catálogo coincidente, y continúa utilizando los atributos de catálogo predeterminados. En este caso, `*`rootId`*` sigue formando parte de la ruta de acceso (que va precedida de `default::RootPath`).

## Propiedades {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Indicador. Establezca el valor en 0 para el comportamiento predeterminado o en 1 para habilitar el comportamiento de coincidencia completa.

## Predeterminado {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Se hereda de `default::FullMatch` si no se ha definido o está vacío.

## Véase también {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
