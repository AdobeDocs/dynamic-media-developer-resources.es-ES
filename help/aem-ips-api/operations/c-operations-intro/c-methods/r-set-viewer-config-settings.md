---
description: Adjunta los ajustes de configuración del visor a un recurso. Pueden ser un ajuste preestablecido de visualizador o el recurso de origen del visualizador.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
TQID: 'https://experienceleague.adobe.com/MX6dj-7j6HfNSISaWFheorOZYVnszSY24OuuUGdKvPA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 12%

---

# setViewerConfigSettings{#setviewerconfigsettings}

Adjunta los ajustes de configuración del visor a un recurso. Pueden ser un ajuste preestablecido de visualizador o el recurso de origen del visualizador.

Sintaxis

## Tipos de usuarios autorizados {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-bcc8c83cc84141e8b1341be9133e8511}

**Entrada (setViewerConfigSettingsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Gestionar en la empresa. |
| assetHandle | `xsd:string` | Sí | Controlador de recurso. |
| nombre | `xsd:string` | Sí | Nombre del recurso. |
| tipo | `xsd:string` | Sí | El tipo de recurso al que desea aplicar la configuración del visor. |
| configSettingArray | `types:ConfigSettingArray` | Sí | La matriz de `ConfigSettings` aplicada al recurso. |

**Salida (setViewerConfigSettingsParam)**

La API de IPS no devuelve una respuesta para esta operación.

