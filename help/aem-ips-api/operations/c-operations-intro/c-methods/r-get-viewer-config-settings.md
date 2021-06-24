---
description: Obtiene todos los ajustes de configuración del visor asociados al recurso especificado.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,ajustes preestablecidos de visor
role: Developer,Administrator
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---

# getViewerConfigSettings{#getviewerconfigsettings}

Obtiene todos los ajustes de configuración del visor asociados al recurso especificado.

Sintaxis

## Tipos de usuarios autorizados {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-7d06abf3d707494c8a1270c7fa1477f1}

**Entrada (getViewerConfigSettingsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Gestionar a la empresa. |
| `*`assetHandle`*` | `xsd:string` | Sí | Gestionar en el recurso. |

**Salida (getViewerCoinfigSettingsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`type`*` | `xsd:string` | Sí | Tipo de visor al que se aplican los ajustes de configuración. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | Sí | Matriz de ajustes de configuración del visor. |
