---
description: Las entradas de caché se actualizan automáticamente mediante la validación de caché basada en catálogo o en caducidad, tal como se selecciona con el atributo CacheValidationPolicy (en default.ini o en el archivo .ini de un catálogo de imágenes específico).
seo-description: Las entradas de caché se actualizan automáticamente mediante la validación de caché basada en catálogo o en caducidad, tal como se selecciona con el atributo CacheValidationPolicy (en default.ini o en el archivo .ini de un catálogo de imágenes específico).
seo-title: Validación de caché de respuesta
solution: Experience Manager
title: Validación de caché de respuesta
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---


# Validación de caché de respuesta{#response-cache-validation}

Las entradas de caché se actualizan automáticamente mediante la validación de caché basada en catálogo o en caducidad, tal como se selecciona con el atributo::CacheValidationPolicy (en default.ini o el archivo .ini de un catálogo de imágenes específico).

Con la validación basada en el catálogo, una entrada de caché existente se considera obsoleta si `catalog::LastModified` (o `attribute::LastModified`, o el tiempo de modificación del archivo del archivo [!DNL catalog.ini]) es más reciente que el momento en que se creó la entrada de caché.

Con la validación basada en la caducidad, una entrada de caché se queda obsoleta después de 5 minutos desde la validación más reciente. En ambos casos, el servidor valida las entradas de caché obsoletas comprobando las fechas del archivo de todos los archivos de imagen implicados en la creación de la solicitud. Si las fechas del archivo no han cambiado, la marca de tiempo de la entrada de caché se actualiza y la fecha en caché se considera válida.

Para aplicaciones típicas que implican principalmente imágenes registradas en catálogos de imágenes, la validación basada en catálogos proporciona una ventaja de rendimiento. Las aplicaciones que no involucran catálogos de imágenes deben utilizar validación de caché basada en caducidad. Una forma de lograrlo es establecer `attribute::cacheValidationPolicy=0` en [!DNL default.ini] y en `1` en todos los archivos de catálogo de imágenes específicos.

Las entradas de caché pasan a ser no válidas y están sujetas a regeneración cuando una entrada de catálogo involucrada en la solicitud cambia de una manera que probablemente provoque un cambio en la imagen de respuesta. Por ejemplo, el contenido de `catalog::Modifier` cambia.

>[!NOTE]
>
>Las imágenes TIFF (PTIFF) piramidales de Dynamic Media mantienen la fecha del archivo internamente en el encabezado del archivo para fines de validación. El tiempo de modificación del archivo que mantiene el sistema de archivos se utiliza para comprobar si un archivo que no es PTIFF ha cambiado.

Solo los archivos de imagen participan en el proceso de validación de la caché. Los cambios en los archivos de fuente o en los archivos de perfil ICC no provocan la invalidación automática de las entradas de caché.
