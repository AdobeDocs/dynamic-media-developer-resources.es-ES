---
description: 'Solo para uso interno. Consulte la sección Referencia del catálogo de materiales para procesamiento de imágenes: Atributos del catálogo.'
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
TQID: 'https://experienceleague.adobe.com/-zBv9N9COcH6KjyHfgjYF4TXblntNiZMVBB6nr-oe2w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 17%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Solo para uso interno. Consulte la sección Referencia del catálogo de materiales para procesamiento de imágenes: Atributos del catálogo.

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
| companyHandle | `xsd:string` | Sí | El identificador de la empresa cuya configuración de publicación de procesamiento de imágenes desea obtener. |
| contextHandle | `xsd:string` | Sí | Administrar en el contexto de publicación. |

**Salida (getImageRenderingPublishSettingsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| publishSettingsArray | `type:ConfigSettingArray` | Sí | Configuración de publicación para procesamiento de imágenes. |
