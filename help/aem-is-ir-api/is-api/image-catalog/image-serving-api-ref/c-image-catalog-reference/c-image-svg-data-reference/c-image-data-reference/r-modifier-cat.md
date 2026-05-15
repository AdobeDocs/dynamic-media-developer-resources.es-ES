---
description: Cadena de modificador de solicitud de prefijo. Ninguno o más comandos del servicio de imágenes separados por caracteres "&".
solution: Experience Manager
title: Modificador
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
TQID: 'https://experienceleague.adobe.com/b1j5WmY-PNOt1zW9qglJob5W8csmI3TidhDwoHK3kCM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 7%

---

# Modificador{#modifier}

Cadena de modificador de solicitud de prefijo. Ninguno o más comandos del servicio de imágenes separados por caracteres &quot;&amp;&quot;.

Se utiliza para modificar imágenes de forma persistente y almacenar el cuerpo de las plantillas.

Los comandos de este campo son reemplazados por los mismos comandos de la solicitud o plantilla desde la que se hace referencia a este registro, y por comandos de `catalog::PostModifier`

Las macros están permitidas en `catalog::Modifier`, siempre y cuando se definan en el mismo catálogo o en el catálogo predeterminado. También se pueden utilizar variables personalizadas.

## Propiedades {#section-6674388f77d644469371a17e8809c45f}

Cadena de texto. Opcional.

## Predeterminado {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Ninguno.

## Véase también {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
