---
description: Trabajo programado para ejecutarse.
seo-description: Trabajo programado para ejecutarse.
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 4%

---


# ScheduledJob{#scheduledjob}

Trabajo programado para ejecutarse.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Identificador de la empresa. |
| `*`jobHandle`*` | `xsd:string` | Control de trabajo programado. |
| `*`name`*` | `xsd:string` | Nombre de trabajo. |
| `*`originalName`*` | `xsd:string` | Nombre original del trabajo programado. |
| `*`type`*` | `xsd:string` | Tipo de trabajo. |
| `*`submitUserEmail`*` | `xsd:string` | La dirección de correo electrónico del usuario que programó el trabajo. |
| `*`locale`*` | `xsd:string` | La configuración regional que se utilizará para los detalles del registro de trabajos y la localización del correo electrónico. Las configuraciones regionales se especifican como `<language_code>[- <country_code>]`, donde el código de idioma es un código de dos letras en minúscula, según se especifica en ISO-639, y el código de país opcional es un código de dos letras en mayúsculas, según se especifica en ISO-3166. Por ejemplo, la cadena de configuración regional para inglés (Estados Unidos) sería: `en-US`. |
| `*`descripción`*` | `xsd:string` | Descripción del trabajo tal como se especificó originalmente en `submitJob`. |
| `*`execSchedule`*` | `xsd:string` | Cuando está programado que se ejecute el trabajo. |
| `*`nextFireTime`*` | `xsd:dateTime` | La fecha, la hora y la zona horaria en la que se activará el trabajo. |
| `*`timeZone`*` | `xsd:dateTime` | Zona horaria del trabajo programado. |
| `*`triggerState`*` | `xsd:int` | Elección del estado de déclencheur del trabajo. |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Detalles de trabajo para un trabajo de publicación de servicio de imágenes. |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Detalles de trabajo para un trabajo de renderización de imágenes. |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | Detalles de trabajo para un trabajo de publicación de vídeo. Consulte [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Detalles de trabajo para un trabajo de publicación de directorio de servidor. |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Detalles del trabajo de un trabajo de directorio de carga. |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | Detalles del trabajo de un trabajo de carga de URL. |
| `*`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | Permitir la exportación autorizada de archivos cargados anteriormente. Consulte [Exportar trabajo](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Notas {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Cuando especifica un valor de tipo de trabajo en `submitJob`, el sistema devuelve un trabajo basado en ese tipo. Se pueden devolver los siguientes trabajos:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

