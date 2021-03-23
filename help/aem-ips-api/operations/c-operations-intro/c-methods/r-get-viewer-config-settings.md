---
description: Obtiene todos los ajustes de configuración del visor asociados al recurso especificado.
seo-description: Obtiene todos los ajustes de configuración del visor asociados al recurso especificado.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
feature: Dynamic Media Classic,SDK/API,ajustes preestablecidos de visor
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 17%

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

