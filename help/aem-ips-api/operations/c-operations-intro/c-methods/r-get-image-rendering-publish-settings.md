---
description: Solo para uso interno. Consulte la sección Referencia del catálogo de material de renderización de imágenes - Atributos del catálogo .
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 16%

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

