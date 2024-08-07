---
description: Obtiene las rutas de acceso al archivo original de los recursos de una empresa.
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 14%

---

# getOriginalFilePaths{#getoriginalfilepaths}

Obtiene las rutas de acceso al archivo original de los recursos de una empresa.

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
| companyHandle | `xsd:string` | Sí | El identificador de la compañía. |
| assetHandleArray | `types:HandleArray` | Sí | Matriz de identificadores de recursos cuya ruta de archivo original desea obtener. |

**Salida (getOriginalFilePathsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| originalFileArray | `types:StringArray` | Sí | Matriz de cadenas que representan las rutas de acceso del archivo original. |

## Ejemplos {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Este ejemplo de código devuelve las rutas de archivo de los recursos especificados con identificadores de recursos únicos en una matriz de identificadores de recursos.

**Solicitud**

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
