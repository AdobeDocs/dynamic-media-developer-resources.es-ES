---
description: Obtiene todos los ajustes de configuración del visor asociados al recurso especificado.
seo-description: Obtiene todos los ajustes de configuración del visor asociados al recurso especificado.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 18%

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
| `*`companyHandle`*` | `xsd:string` | Sí | Manejar a la compañía. |
| `*`assetHandle`*` | `xsd:string` | Sí | Gestionar en el recurso. |

**Salida (getViewerCoinfigSettingsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`type`*` | `xsd:string` | Sí | Tipo de visor al que se aplican las opciones de configuración. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | Sí | Matriz de los ajustes de configuración del visor. |

