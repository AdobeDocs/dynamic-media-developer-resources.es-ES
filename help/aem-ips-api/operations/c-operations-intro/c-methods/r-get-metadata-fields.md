---
description: Obtiene los campos de metadatos definidos por el usuario asociados a un recurso.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 15%

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
| companyHandle | `xsd:string` | Sí | El control de la empresa. |
| assetType | `xsd:string` | Sí | Tipos de recursos de los que obtener metadatos. |

**Salida (getMetadataFieldsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| Frase de código | `Code Phrase` |  |  |

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
