---
description: Obtiene las rutas de archivo originales de los recursos de una empresa.
seo-description: Obtiene las rutas de archivo originales de los recursos de una empresa.
seo-title: getOriginalFilePaths
solution: Experience Manager
title: getOriginalFilePaths
uuid: c4acf288-1a57-4295-806b-348f15a089cc
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 13%

---


# getOriginalFilePaths{#getoriginalfilepaths}

Obtiene las rutas de archivo originales de los recursos de una empresa.

Sintaxis

## Tipos de usuarios autorizados {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Requiere acceso de lectura al recurso.

## Parámetros {#section-a6b394daba6e49a8882cf3051035d9d1}

**Entrada (getOriginalFilePathsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sí | Matriz de identificadores a recursos cuya ruta de archivo original desea obtener. |

**Salida (getOriginalFilePathsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`originalFileArray`*` | `types:StringArray` | Sí | Matriz de cadenas que representan las rutas de archivo originales. |

## Ejemplos {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Este ejemplo de código devuelve las rutas de archivos de los recursos especificados con controladores de recursos únicos en una matriz de gestión de recursos.

**Solicitar**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**Respuesta**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```

