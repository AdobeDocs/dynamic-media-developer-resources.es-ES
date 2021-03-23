---
description: 'Solo para uso interno. Los usuarios deben consultar la sección Referencia del catálogo de imágenes de servicio de imágenes: Referencia de atributos .'
seo-description: 'Solo para uso interno. Los usuarios deben consultar la sección Referencia del catálogo de imágenes de servicio de imágenes: Referencia de atributos .'
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 12%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Solo para uso interno. Los usuarios deben consultar la sección Referencia del catálogo de imágenes de servicio de imágenes: Referencia de atributos .

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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con la imagen que sirve para la configuración de publicación. |
| `*`contextHandle`*` | `xsd:string` | Sí | Gestionar en el contexto de publicación. |

**Salida**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | Sí | Matriz de configuración de publicación del servidor de imágenes. |

