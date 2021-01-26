---
description: Adjunta la configuración del visor a un recurso. Puede ser un ajuste preestablecido de visor o el recurso de origen para el visor.
seo-description: Adjunta la configuración del visor a un recurso. Puede ser un ajuste preestablecido de visor o el recurso de origen para el visor.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: d83d866e-9243-479f-9b33-727aad8158e5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 10%

---


# setViewerConfigSettings{#setviewerconfigsettings}

Adjunta la configuración del visor a un recurso. Puede ser un ajuste preestablecido de visor o el recurso de origen para el visor.

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
| `*`companyHandle`*` | `xsd:string` | Sí | Manejar a la compañía. |
| `*`assetHandle`*` | `xsd:string` | Sí | Identificador de recurso. |
| `*`name`*` | `xsd:string` | Sí | Nombre del recurso. |
| `*`type`*` | `xsd:string` | Sí | Tipo de recurso al que desea aplicar la configuración del visor. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Sí | Matriz de `ConfigSettings` aplicada al recurso. |

**Salida (setViewerConfigSettingsParam)**

La API de IPS no devuelve una respuesta para esta operación.
