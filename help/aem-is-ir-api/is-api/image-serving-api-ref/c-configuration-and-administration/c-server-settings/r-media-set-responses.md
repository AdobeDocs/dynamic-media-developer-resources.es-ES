---
title: Respuestas del conjunto de medios
description: La configuración de esta sección se aplica a las respuestas del conjunto de medios obtenidas por el modificador req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Respuestas del conjunto de medios{#media-set-responses}

La configuración de esta sección se aplica a las respuestas del conjunto de medios obtenidas por el `req=set` modificador.

## PS::fvctx.useCatalogRecordValidation: directiva de almacenamiento en caché {#section-9accb087d16548a988993bb30395a6f6}

Esta propiedad controla la directiva de almacenamiento en caché al determinar si se debe volver a generar una respuesta establecida recuperada de una caché. Si la propiedad está deshabilitada, la marca de tiempo del [!DNL catalog.ini] se utiliza para la validación. Si la propiedad está habilitada, se recomienda la última `catalog::LastModified` para la validación se utiliza la marca de tiempo de todos los registros a los que se hace referencia.

## PS::fvctx.nestingLimit: límite de anidación {#section-280210341f1647fea02590e7069934d2}

Profundidad máxima de anidación de cualquier `req=set` respuesta. Si se supera esta profundidad, se devuelve un error.

## PS::fvctx.brochureLimit: límite de catálogos {#section-fe36e47db49244cea7f07e9dd3639440}

El número máximo de catálogos electrónicos en el `req=set` Respuesta que contiene todos los metadatos asociados. Una vez superado este límite, se suprimen los mapas privados y los datos de usuario asociados con el elemento del folleto.
