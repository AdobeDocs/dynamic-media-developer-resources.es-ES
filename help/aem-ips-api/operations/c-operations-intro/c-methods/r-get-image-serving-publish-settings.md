---
description: 'Solo para uso interno. Los usuarios deben consultar la sección Referencia del catálogo de imágenes de servicio de imágenes: Referencia de atributos .'
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 14%

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

