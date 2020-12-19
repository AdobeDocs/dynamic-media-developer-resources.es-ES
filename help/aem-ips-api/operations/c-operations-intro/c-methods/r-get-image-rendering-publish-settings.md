---
description: 'Solo para uso interno. Consulte la sección Referencia del catálogo de materiales de procesamiento de imágenes: Atributos del catálogo.'
seo-description: 'Solo para uso interno. Consulte la sección Referencia del catálogo de materiales de procesamiento de imágenes: Atributos del catálogo.'
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
topic: Scene7 Image Production System API
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 14%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Solo para uso interno. Consulte la sección Referencia del catálogo de materiales de procesamiento de imágenes: Atributos del catálogo.

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía cuya configuración de publicación de procesamiento de imágenes desee obtener. |
| ` *`contextHandle`*` | `xsd:string` | Sí | Gestionar en el contexto de publicación. |

**Salida (getImageRenderingPublishSettingsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`publishSettingsArray`*` | `type:ConfigSettingArray` | Sí | Configuración de publicación de procesamiento de imágenes. |

