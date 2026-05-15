---
description: Las entradas de caché se actualizan automáticamente mediante la validación de caché basada en el catálogo o en la caducidad, tal como se selecciona con el atributo CacheValidationPolicy (en default.ini o el archivo .ini de un catálogo de imágenes específico).
solution: Experience Manager
title: Validación de caché de respuestas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
TQID: 'https://experienceleague.adobe.com/VnvYNkc3yijayG8tnJKHsp94Qto8VZj9OkIgfIv1Kc0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 311
ht-degree: 0%

---

# Validación de caché de respuestas{#response-cache-validation}

Las entradas de caché se actualizan automáticamente mediante la validación de caché basada en el catálogo o en la caducidad, tal como se selecciona con attribute::CacheValidationPolicy (en default.ini o el archivo .ini de un catálogo de imágenes específico).

Con la validación basada en el catálogo, una entrada de caché existente se considera obsoleta si `catalog::LastModified` (o `attribute::LastModified`, o la hora de modificación del archivo [!DNL catalog.ini]) es más reciente que la hora en la que se creó la entrada de caché.

Con la validación basada en la caducidad, una entrada de caché queda obsoleta pasados 5 minutos desde la validación más reciente. En ambos casos, el servidor valida las entradas de caché obsoletas comprobando las fechas de los archivos de imagen que se utilizaron para crear la solicitud. Si las fechas del archivo no han cambiado, la marca de tiempo de la entrada de caché se actualiza y la fecha en caché se considera válida.

Para las aplicaciones típicas que implican principalmente imágenes registradas en catálogos de imágenes, la validación basada en catálogos proporciona una ventaja de rendimiento. Las aplicaciones que no implican catálogos de imágenes deben utilizar la validación de caché basada en la caducidad. Una manera de conseguirlo es establecer `attribute::cacheValidationPolicy=0` en [!DNL default.ini] y `1` en todos los archivos específicos del catálogo de imágenes.

Las entradas de caché dejan de ser válidas y están sujetas a regeneración cuando una entrada de catálogo relacionada con la solicitud cambia de una manera que probablemente causaría un cambio en la imagen de respuesta. Por ejemplo, cambia el contenido de `catalog::Modifier`.

>[!NOTE]
>
>Las imágenes de TIFF piramidal de Dynamic Media (PTIFF) mantienen la fecha del archivo internamente en el encabezado del archivo con fines de validación. El tiempo de modificación del archivo mantenido por el sistema de archivos se utiliza para comprobar si ha cambiado un archivo que no es PTIFF.

Solo los archivos de imagen participan en el proceso de validación de caché. Los cambios en los archivos de fuente o en los archivos de perfil ICC no provocan la invalidación automática de las entradas de la caché.
