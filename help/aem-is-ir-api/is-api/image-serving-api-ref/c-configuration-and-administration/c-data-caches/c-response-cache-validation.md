---
description: Las entradas de caché se actualizan automáticamente mediante validación de caché basada en catálogo o en caducidad, tal como se selecciona con el atributo CacheValidationPolicy (en default.ini o en el archivo .ini de un catálogo de imágenes específico).
seo-description: Las entradas de caché se actualizan automáticamente mediante validación de caché basada en catálogo o en caducidad, tal como se selecciona con el atributo CacheValidationPolicy (en default.ini o en el archivo .ini de un catálogo de imágenes específico).
seo-title: Validación de caché de respuesta
solution: Experience Manager
title: Validación de caché de respuesta
topic: Scene7 Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# Validación de caché de respuesta{#response-cache-validation}

Las entradas de caché se actualizan automáticamente mediante validación de caché basada en catálogo o en caducidad, tal como se selecciona con el atributo::CacheValidationPolicy (en default.ini o en el archivo .ini de un catálogo de imágenes específico).

Con la validación basada en catálogo, una entrada de caché existente se considera obsoleta si `catalog::LastModified` (o `attribute::LastModified`, o el tiempo de modificación del archivo del [!DNL catalog.ini] archivo) es más reciente que el momento en que se creó la entrada de caché.

Con la validación basada en la caducidad, una entrada de caché se queda obsoleta pasados 5 minutos desde la validación más reciente. En ambos casos, el servidor valida las entradas de caché antiguas comprobando las fechas de archivo de todos los archivos de imagen que participaron en la creación de la solicitud. Si las fechas del archivo no han cambiado, la marca de hora de la entrada de caché se actualiza y la fecha en caché se considera válida.

Para aplicaciones típicas que involucran principalmente imágenes registradas en catálogos de imágenes, la validación basada en catálogos ofrece una ventaja de rendimiento. Las aplicaciones que no incluyan catálogos de imágenes deben utilizar la validación de caché basada en la caducidad. Una manera de lograrlo es configurarlo `attribute::cacheValidationPolicy=0` en [!DNL default.ini]todos los archivos de catálogo de imágenes específicos y `1` en todos ellos.

Las entradas de caché pasan a ser no válidas y están sujetas a regeneración cuando una entrada de catálogo que participa en la solicitud cambia de forma que probablemente provocaría un cambio en la imagen de respuesta. Por ejemplo, el contenido de los `catalog::Modifier` cambios.

>[!NOTE]
>
>Las imágenes TIFF (PTIFF) piramidales de Scene7 mantienen la fecha del archivo internamente en el encabezado del archivo para fines de validación. El tiempo de modificación del archivo que mantiene el sistema de archivos se utiliza para comprobar si un archivo que no es PTIFF ha cambiado.

Solo los archivos de imagen participan en el proceso de validación de caché. Los cambios en los archivos de fuente o en los archivos de perfil ICC no invalidan automáticamente las entradas de caché.
