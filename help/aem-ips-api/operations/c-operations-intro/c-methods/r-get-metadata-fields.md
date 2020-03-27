---
description: Obtiene los campos de metadatos definidos por el usuario asociados a un recurso.
seo-description: Obtiene los campos de metadatos definidos por el usuario asociados a un recurso.
seo-title: getMetadataFields
solution: Experience Manager
title: getMetadataFields
topic: Scene7 Image Production System API
uuid: bf891bae-53c8-4e3d-90df-caca9a7e022b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sí | El identificador de compañía. |
| ` *`assetType`*` | `xsd:string` | Sí | Tipos de recursos de los que obtener metadatos. |

**Salida (getMetadataFieldsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`Frase de código`*` | `Code Phrase` |  |  |

## Ejemplos {#section-dbfde1483d614b5aac2b491cb32115d7}

Este ejemplo de código devuelve recursos de metadatos para el tipo y la compañía especificados. La respuesta contiene una matriz de campos de metadatos en una matriz de campos. No todos los recursos tienen los mismos metadatos. El usuario de IPS define el campo de metadatos del recurso.

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

