---
description: Trabajo que está programado para ejecutarse.
seo-description: Trabajo que está programado para ejecutarse.
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Scene7 Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 4%

---


# ScheduledJob{#scheduledjob}

Trabajo que está programado para ejecutarse.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Identificador de Compañía. |
| ` *`jobHandle`*` | `xsd:string` | Identificador de trabajo programado. |
| ` *`name`*` | `xsd:string` | Nombre de trabajo. |
| ` *`originalName`*` | `xsd:string` | Nombre original del trabajo programado. |
| ` *`type`*` | `xsd:string` | Tipo de trabajo. |
| ` *`submitUserEmail`*` | `xsd:string` | La dirección de correo electrónico del usuario que programó el trabajo. |
| ` *`locale`*` | `xsd:string` | La configuración regional que se utilizará para los detalles del registro de trabajos y la localización por correo electrónico. Las configuraciones regionales se especifican como `<language_code>[- <country_code>]`, donde el código de idioma es un código de dos letras en minúscula según lo especificado por ISO-639, y el código de país opcional es un código de dos letras en mayúsculas según lo especificado por ISO-3166. Por ejemplo, la cadena de configuración regional para inglés (Estados Unidos) sería: `en-US`. |
| ` *`description`*` | `xsd:string` | Descripción del trabajo tal como se especificó originalmente en `submitJob`. |
| ` *`execSchedule`*` | `xsd:string` | Cuándo se programó la ejecución del trabajo. |
| ` *`nextFireTime`*` | `xsd:dateTime` | Fecha, hora y zona horaria en que se activará el trabajo. |
| ` *`timeZone`*` | `xsd:dateTime` | Huso horario del trabajo programado. |
| ` *`desencadenadorEstado`*` | `xsd:int` | Opción del estado desencadenador del trabajo. |
| ` *`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Detalles del trabajo de un trabajo de publicación de servicio de imágenes. |
| ` *`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Detalles del trabajo de un trabajo de procesamiento de imágenes. |
| ` *`videoPublishJob`*` | `types:VideoPublishJob` | Detalles del trabajo de un trabajo de publicación de vídeo. Consulte [VideoPublishJob](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| ` *`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Detalles del trabajo de un trabajo de publicación de directorio de servidor. |
| ` *`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Detalles del trabajo de un trabajo de directorio de carga. |
| ` *`uploadUrlsJob`*` | `types:UploadUrlsJob` | Detalles del trabajo de un trabajo de URL de carga. |
| ` *`optimizedImagesJob`*` | `types:OptimizeImagesJob` |  |
| ` *`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| ` *`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| ` *`exportJob`*` | `types:ExportJob` | Permitir la exportación autorizada de archivos cargados anteriormente. Consulte Trabajo [de exportación](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Notas {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Cuando se especifica un valor de tipo de trabajo en `submitJob`, el sistema devuelve un trabajo basado en ese tipo. Se pueden devolver los siguientes trabajos:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

