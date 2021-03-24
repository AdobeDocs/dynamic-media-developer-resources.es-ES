---
description: La configuración de esta sección se aplica a las respuestas del conjunto de medios obtenidas por el modificador req=set.
solution: Experience Manager
title: Respuestas de conjuntos de medios
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Respuestas de conjuntos de medios{#media-set-responses}

La configuración de esta sección se aplica a las respuestas del conjunto de medios obtenidas por el modificador req=set.

## PS::fvctx.useCatalogRecordValidation - Política de almacenamiento en caché {#section-9accb087d16548a988993bb30395a6f6}

Esta propiedad controla la directiva de almacenamiento en caché al determinar si se debe volver a generar la respuesta recuperada de la caché o no. Si la propiedad está deshabilitada, la marca de tiempo del archivo [!DNL catalog.ini] se utiliza para la validación. Si la propiedad está habilitada, la última `catalog::LastModified` marca de tiempo de todos los registros a los que se hace referencia se utiliza para la validación.

## PS::fvctx.nestedLimit - Límite de anidación {#section-280210341f1647fea02590e7069934d2}

Profundidad máxima de anidación de cualquier respuesta `req=set`. Si se supera esta profundidad, se devuelve un error.

## PS::fvctx.folureLimit - Límite de folletos {#section-fe36e47db49244cea7f07e9dd3639440}

El número máximo de folletos de catálogo electrónico en la respuesta `req=set` que contiene todos los metadatos asociados. Una vez superado este límite, se suprimen los mapas privados y los datos de usuario asociados con el elemento de folleto.
