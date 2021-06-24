---
description: Actualiza los ajustes de configuración del visor SWF.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,ajustes preestablecidos de visor
role: Developer,Administrator
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 13%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

Actualiza los ajustes de configuración del visor SWF.

Sintaxis

## Tipos de usuarios autorizados {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-29790d933fb24aa392d0cb2d52d1310f}

**Entrada (updateViewerConfigSettingsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Gestionar a la empresa. |
| `*`assetHandle`*` | `xsd:string` | Sí | Identificador de recurso. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Sí | Matriz de ajustes de configuración que desea aplicar al visor. |

**Salida (updateViewerConfigSettingsReturn)**

La API IPS no devuelve una respuesta para esta operación.
