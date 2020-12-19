---
description: Devuelve todos los valores de un campo de metadatos.
seo-description: Devuelve todos los valores de un campo de metadatos.
seo-title: getDistinctMetadataValues
solution: Experience Manager
title: getDistinctMetadataValues
topic: Scene7 Image Production System API
uuid: 47c1d3a3-9f33-4c36-828a-e858370997d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 21%

---


# getDistinctMetadataValues{#getdistinctmetadatavalues}

Devuelve todos los valores de un campo de metadatos.

Sintaxis

## Tipos de usuarios autorizados {#section-f0f44fdcb318490582dd04de8eaf745d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-600f36a32ff147cb83149943d37843e2}

**Input (getDistinctMetadataValuesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía para la que desea obtener datos. |
| ` *`metadataKey`*` | `xsd:string` | Sí | Clave de metadatos en notación de puntos. |

**Salida (getDistinctMetadataValuesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`valueArray`*` | `types:ValueArray` | Sí | Valores del campo de metadatos solicitado. |

## Ejemplos {#section-0189fa6fb31646cda5ce1b0bc4fcdf46}

**Solicitar**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
         <xsd:user>user@company.com</xsd:user>
         <xsd:password>password</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
   <ns:getDistinctMetadataValuesParam>
      <ns:companyHandle>680</ns:companyHandle>
      <ns:metadataKey>dc.format</ns:metadataKey>
      </ns:getDistinctMetadataValuesParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Respuesta**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <getDistinctMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <valueArray>
            <items>
               <value>N/A</value>
               <count>412</count>
            </items>
            <items>
               <value>image/jpeg</value>
               <count>189</count>
            </items>
            <items>
               <value>image/epsf</value>
               <count>1</count>
            </items>
            <items>
               <value>image/tiff</value>
               <count>3</count>
            </items>
         </valueArray>
      </getDistinctMetadataValuesReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

