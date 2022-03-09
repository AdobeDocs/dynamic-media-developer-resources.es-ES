---
description: Devuelve todos los campos de metadatos agrupados por tipo de recurso.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 23%

---

# getAssetMetadataFields{#getassetmetadatafields}

Devuelve todos los campos de metadatos agrupados por tipo de recurso.

Sintaxis

## Tipos de usuarios autorizados {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**Entrada (getAssetMetadataFieldsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Identificador de la empresa cuyos metadatos desea recuperar. |

**Salida (getAssetMetadataFieldsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | Sí | Matriz de campos de metadatos, por tipo de recurso. |

## Ejemplos {#section-d79ab85f29144635b0b61416e52f4f3f}

**Solicitar**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Respuesta**

>[!NOTE]
>
>Truncado para la brevedad.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
