---
description: Adjunta los ajustes de configuración del visor a un recurso. Pueden ser un ajuste preestablecido de visualizador o el recurso de origen para el visualizador.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,ajustes preestablecidos de visor
role: Developer,Administrator
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 11%

---

# setViewerConfigSettings{#setviewerconfigsettings}

Adjunta los ajustes de configuración del visor a un recurso. Pueden ser un ajuste preestablecido de visualizador o el recurso de origen para el visualizador.

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
| `*`companyHandle`*` | `xsd:string` | Sí | Gestionar a la empresa. |
| `*`assetHandle`*` | `xsd:string` | Sí | Identificador de recurso. |
| `*`name`*` | `xsd:string` | Sí | Nombre del recurso. |
| `*`type`*` | `xsd:string` | Sí | Tipo de recurso al que desea aplicar la configuración del visor. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Sí | La matriz de `ConfigSettings` aplicada al recurso. |

**Salida (setViewerConfigSettingsParam)**

La API IPS no devuelve una respuesta para esta operación.
