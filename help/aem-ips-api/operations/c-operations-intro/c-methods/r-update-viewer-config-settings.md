---
description: Actualiza la configuración del visor SWF.
seo-description: Actualiza la configuración del visor SWF.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
topic: Scene7 Image Production System API
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateViewerConfigSettings{#updateviewerconfigsettings}

Actualiza la configuración del visor SWF.

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Manejar a la compañía. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador de recurso. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | Sí | Matriz de opciones de configuración que desea aplicar al visor. |

**Salida (updateViewerConfigSettingsReturn)**

La API de IPS no devuelve una respuesta para esta operación.
