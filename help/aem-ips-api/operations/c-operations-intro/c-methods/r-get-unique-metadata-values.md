---
description: Obtiene valores de campo de metadatos únicos.
seo-description: Obtiene valores de campo de metadatos únicos.
seo-title: getUniqueMetadataValues
solution: Experience Manager
title: getUniqueMetadataValues
topic: Scene7 Image Production System API
uuid: 5b2f95a7-cc0b-4938-99b9-2aefa0ffe693
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

Obtiene valores de campo de metadatos únicos.

Sintaxis

## Tipos de usuarios autorizados {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-b9d1413811c24566b6d095701f0f66db}

**Entrada (getUniqueMetadataValuesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Manejar a la compañía. |
| ` *`fieldHandle`*` | `xsd:string` | No | Controlar el campo de metadatos. |

**Salida (getUniqueMetadataValuesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`values`*` | `type:StringArray` |  |  |

## Ejemplos {#section-440f3bc3e5be436cb6ec26117d05f476}

Este ejemplo de código utiliza un identificador de campo para devolver valores de metadatos específicos.

**Solicitar**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Respuesta**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

