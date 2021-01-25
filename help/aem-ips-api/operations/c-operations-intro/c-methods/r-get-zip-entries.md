---
description: Devuelve datos de archivo Zip.
seo-description: Devuelve datos de archivo Zip.
seo-title: getZipEntries
solution: Experience Manager
title: getZipEntries
topic: Dynamic Media Image Production System API
uuid: cfc45f83-1cf9-4c50-9aac-5a731e62a839
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 21%

---


# getZipEntries{#getzipentries}

Devuelve datos de archivo Zip.

Sintaxis

## Tipos de usuarios autorizados {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-aa3f498fe76d4a5f99c42d64520fadce}

**Entrada (getZipEntriesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que contiene el archivo Zip. |
| `*`assetHandle`*` | `xsd:string` | Sí | Administre el archivo Zip. |

**Salida (getZipEntriesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | Sí | Matriz de entradas en un archivo Zip. |

## Ejemplos {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Este ejemplo de código devuelve información del archivo Zip, incluido el tamaño comprimido y sin comprimir.

**Solicitar**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**Respuesta**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```

