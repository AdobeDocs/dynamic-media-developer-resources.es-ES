---
description: Anclaje de imagen. Punto de origen cuando esta imagen se utiliza como capa en una plantilla o imagen compuesta.
solution: Experience Manager
title: Anclaje
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
TQID: 'https://experienceleague.adobe.com/OKTbXTF3uzVcQeLQIGIJhCukQFzdW5gZMzatSdWP7yY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 4%

---

# Anclaje{#anchor}

Anclaje de imagen. Punto de origen cuando esta imagen se utiliza como capa en una plantilla o imagen compuesta.

Define también el punto central por defecto para la rotación.

## Propiedades {#section-95740f14160744e7bc763094b8be40d8}

Dos números enteros, separados por una coma. Desplazamiento de píxel relativo a la esquina superior izquierda de la imagen de resolución completa.

Anulado por `anchor=` (que a su vez se puede anular con `origin=`).

## Predeterminado {#section-ca3a4cc837d643519eff15951f2b47a1}

El punto central de la imagen se utiliza si este campo no está presente o si está vacío, y si es un registro de imagen válido (es decir, si `catalog::Path` es válido).

## Véase también {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anclaje=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origen=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
