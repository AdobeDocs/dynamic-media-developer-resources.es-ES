---
description: La configuración de esta sección se aplica a las respuestas de conjuntos de medios obtenidas por el modificador req=set.
seo-description: La configuración de esta sección se aplica a las respuestas de conjuntos de medios obtenidas por el modificador req=set.
seo-title: Respuestas al conjunto de medios
solution: Experience Manager
title: Respuestas al conjunto de medios
topic: Scene7 Image Serving - Image Rendering API
uuid: 9fa6a38a-cd1f-499b-a2b6-e1a9a6c69ed0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Respuestas al conjunto de medios{#media-set-responses}

La configuración de esta sección se aplica a las respuestas de conjuntos de medios obtenidas por el modificador req=set.

## PS::fvctx.useCatalogRecordValidation - Política de almacenamiento en caché {#section-9accb087d16548a988993bb30395a6f6}

Esta propiedad controla la directiva de almacenamiento en caché al determinar si es necesario volver a generar la respuesta recuperada de la caché o no. Si la propiedad está deshabilitada, la marca de tiempo del [!DNL catalog.ini] archivo se utiliza para la validación. Si la propiedad está habilitada, se utiliza la última `catalog::LastModified` marca de tiempo de todos los registros a los que se hace referencia para la validación.

## PS::fvctx.nestingLimit: límite de anidación {#section-280210341f1647fea02590e7069934d2}

Profundidad máxima de anidación de cualquier `req=set` respuesta. Si se supera esta profundidad, se mostrará un error.

## PS::fvctx.folureLimit: límite de folletos {#section-fe36e47db49244cea7f07e9dd3639440}

El número máximo de folletos de catálogo electrónico en la `req=set` respuesta que contiene todos los metadatos asociados. Una vez superado este límite, se suprimen los mapas privados y los datos de usuario asociados con el elemento de folleto.
