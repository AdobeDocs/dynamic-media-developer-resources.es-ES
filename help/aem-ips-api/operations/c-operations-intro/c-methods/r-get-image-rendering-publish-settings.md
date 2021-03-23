---
description: Solo para uso interno. Consulte la sección Referencia del catálogo de material de renderización de imágenes - Atributos del catálogo .
seo-description: Solo para uso interno. Consulte la sección Referencia del catálogo de material de renderización de imágenes - Atributos del catálogo .
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 13%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Solo para uso interno. Consulte la sección Referencia del catálogo de material de renderización de imágenes - Atributos del catálogo .

Sintaxis

## Tipos de usuarios autorizados {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-4f2cb8c589384816bb2525654ec49963}

**Entrada (getImageRenderingPublishSettingsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa cuya configuración de publicación de procesamiento de imágenes desee obtener. |
| `*`contextHandle`*` | `xsd:string` | Sí | Gestionar en el contexto de publicación. |

**Salida (getImageRenderingPublishSettingsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | Sí | Configuración de publicación de procesamiento de imágenes. |

