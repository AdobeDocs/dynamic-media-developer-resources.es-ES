---
description: 'Solo para uso interno. Los usuarios deben consultar la sección Referencia del catálogo de imágenes del servicio de imágenes: Referencia de atributos.'
seo-description: 'Solo para uso interno. Los usuarios deben consultar la sección Referencia del catálogo de imágenes del servicio de imágenes: Referencia de atributos.'
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Scene7 Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Solo para uso interno. Los usuarios deben consultar la sección Referencia del catálogo de imágenes del servicio de imágenes: Referencia de atributos.

Sintaxis

## Tipos de usuarios autorizados {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-79f0d54acd604ad2a5c96679334f2424}

**Entrada (getImageServingPublishSettingsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con la configuración de publicación del servicio de imágenes. |
| ` *`contextHandle`*` | `xsd:string` | Sí | Gestionar en el contexto de publicación. |

**Salida**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`publishSettingArray`*` | `xsd:string` | Sí | Matriz de la configuración de publicación del servidor de imágenes. |

