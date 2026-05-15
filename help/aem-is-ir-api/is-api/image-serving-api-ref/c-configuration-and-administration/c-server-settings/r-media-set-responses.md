---
title: Respuestas del conjunto de medios
description: La configuración de esta sección se aplica a las respuestas del conjunto de medios obtenidas por el modificador req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
TQID: 'https://experienceleague.adobe.com/FNUguOqf8f5FnIeGTzheZU-8zCXqwRMU3YGyvYDA0uM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 0%

---

# Respuestas del conjunto de medios{#media-set-responses}

La configuración de esta sección se aplica a las respuestas del conjunto de medios obtenidas por el modificador `req=set`.

## PS::fvctx.useCatalogRecordValidation: directiva de almacenamiento en caché {#section-9accb087d16548a988993bb30395a6f6}

Esta propiedad controla la directiva de almacenamiento en caché al determinar si se debe volver a generar una respuesta establecida recuperada de una caché. Si la propiedad está deshabilitada, se usará la marca de tiempo del archivo [!DNL catalog.ini] para la validación. Si la propiedad está habilitada, se utiliza la última marca de tiempo `catalog::LastModified` de todos los registros a los que se hace referencia para la validación.

## PS::fvctx.nestingLimit: límite de anidación {#section-280210341f1647fea02590e7069934d2}

Profundidad máxima de anidación de cualquier respuesta `req=set`. Si se supera esta profundidad, se devuelve un error.

## PS::fvctx.brochureLimit: límite de catálogos {#section-fe36e47db49244cea7f07e9dd3639440}

Número máximo de catálogos electrónicos en la respuesta `req=set` que contiene todos los metadatos asociados. Una vez superado este límite, se suprimen los mapas privados y los datos de usuario asociados con el elemento del folleto.
