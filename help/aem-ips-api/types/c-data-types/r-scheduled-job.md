---
description: Un trabajo programado para ejecutarse.
solution: Experience Manager
title: TrabajoProgramado
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
TQID: 'https://experienceleague.adobe.com/OFG30nHlkuRT7HeNob0hkEfaygi8b2gNFEiu67LJBmU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 276
ht-degree: 3%

---

# [!DNL ScheduledJob]{#scheduledjob}

Un trabajo programado para ejecutarse.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| companyHandle | `xsd:string` | Manejo de la compañía. |
| jobHandle | `xsd:string` | Controlador del trabajo programado. |
| nombre | `xsd:string` | Nombre de trabajo. |
| originalName | `xsd:string` | Nombre original del trabajo programado. |
| tipo | `xsd:string` | Tipo de trabajo. |
| submitUserEmail | `xsd:string` | La dirección de correo electrónico del usuario que programó el trabajo. |
| configuración regional | `xsd:string` | La configuración regional que se utilizará para los detalles del registro de trabajos y la localización por correo electrónico. Las configuraciones regionales se especifican como `<language_code>[- <country_code>]`, donde el código de idioma es un código de dos letras en minúsculas según lo especificado en ISO-639, y el código de país opcional es un código de dos letras en mayúsculas según lo especificado en ISO-3166. Por ejemplo, la cadena de configuración regional para inglés (Estados Unidos) sería: `en-US`. |
| descripción | `xsd:string` | Una descripción del trabajo tal como se especificó originalmente en `submitJob`. |
| execSchedule | `xsd:string` | Cuando el trabajo está programado para ejecutarse. |
| nextFireTime | `xsd:dateTime` | La fecha, la hora y la zona horaria en que se activó el trabajo. |
| timeZone | `xsd:dateTime` | Zona horaria del trabajo programado. |
| triggerState | `xsd:int` | Elección del estado de déclencheur del trabajo. |
| imageServingPublishJob | `types:ImageServingPublishJob` | Detalles de trabajo de un trabajo de publicación para servicio de imágenes. |
| imageServingRenderJob | `types:ImageServingRenderJob` | Detalles del trabajo de un trabajo de renderización de imágenes. |
| videoPublishJob | `types:VideoPublishJob` | Detalles de trabajo de un trabajo de publicación de vídeo. Ver [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | Detalles de trabajo para un trabajo de publicación de directorio de servidor. |
| uploadDirectoryJob | `types:UploadDirectoryJob` | Detalles del trabajo de un trabajo de directorio de carga. |
| uploadUrlsJob | `types:UploadUrlsJob` | Detalles del trabajo de carga de URL. |
| optimizeImagesJob | `types:OptimizeImagesJob` | |
| ripPdfsJob | `types:RipPdfsJob` | |
| reprocessAssetsJob | `types:ReprocessAssetsJob` | |
| exportJob | `types:ExportJob` | Permitir la exportación autorizada de archivos cargados anteriormente. Ver [Trabajo de exportación](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Notas {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Cuando especifica un valor de tipo de trabajo en `submitJob`, el sistema devuelve un trabajo basado en ese tipo. Se pueden devolver los siguientes trabajos:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
