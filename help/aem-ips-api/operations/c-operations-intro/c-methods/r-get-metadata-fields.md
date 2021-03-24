---
description: Obtiene los campos de metadatos definidos por el usuario asociados a un recurso.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadatos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 14%

---


# getMetadataFields{#getmetadatafields}

Obtiene los campos de metadatos definidos por el usuario asociados a un recurso.

Sintaxis

## Tipos de usuarios autorizados {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-bac949e59c0546429c5786fe422d750d}

**Entrada (getMetadataFieldsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El control de la empresa. |
| `*`assetType`*` | `xsd:string` | Sí | Tipos de recursos de los que obtener metadatos. |

**Salida (getMetadataFieldsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`Frase de código`*` | `Code Phrase` |  |  |

## Ejemplos {#section-dbfde1483d614b5aac2b491cb32115d7}

Este ejemplo de código devuelve recursos de metadatos para el tipo y la empresa especificados. La respuesta contiene una matriz de campos de metadatos en una matriz de campos. No todos los recursos tienen los mismos metadatos. El usuario de IPS define el campo de metadatos del recurso.

**Solicitar**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**Respuesta**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```

