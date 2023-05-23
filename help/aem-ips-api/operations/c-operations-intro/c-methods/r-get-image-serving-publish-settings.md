---
description: 'Solo para uso interno. Los usuarios deben consultar la sección Referencia del catálogo de imágenes para servicio de imágenes: referencia de atributos.'
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 16%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

Solo para uso interno. Los usuarios deben consultar la sección Referencia del catálogo de imágenes para servicio de imágenes: referencia de atributos.

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
| companyHandle | `xsd:string` | Sí | El identificador de la empresa con la configuración de publicación del servicio de imágenes. |
| contextHandle | `xsd:string` | Sí | Administrar en el contexto de publicación. |

**Output**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| publishSettingArray | `xsd:string` | Sí | Matriz de configuraciones de publicación del servidor de imágenes. |
