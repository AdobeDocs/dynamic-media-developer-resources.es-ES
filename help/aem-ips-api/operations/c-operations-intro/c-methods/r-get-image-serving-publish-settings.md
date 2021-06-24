---
description: 'Solo para uso interno. Los usuarios deben consultar la sección Referencia del catálogo de imágenes de servicio de imágenes: Referencia de atributos .'
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

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
