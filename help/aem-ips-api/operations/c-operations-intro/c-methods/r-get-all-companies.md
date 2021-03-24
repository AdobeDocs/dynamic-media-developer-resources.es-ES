---
description: Devuelve una matriz de todas las empresas.
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 19%

---


# getAllCompanies{#getallcompanies}

Devuelve una matriz de todas las empresas.

Sintaxis

## Tipos de usuarios autorizados {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## Parámetros {#section-efd74992e6904ebabe7383b577af4fdb}

**Entrada (getAllCompaniesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`includeExpired`*` | `xsd:boolean` | Sí | Configúrelo en true para devolver compañías caducadas y no caducadas. |

**Salida (getAllCompaniesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyArray`*` | `types:CompanyArray` | Sí | La matriz de empresas. |

## Ejemplos {#section-3eecf4e6900b41fb92a0e3214791c6b9}

Este ejemplo de código devuelve todas las empresas en IPS en una matriz. Tenga en cuenta que la respuesta de ejemplo se trunca para su brevedad.

**Solicitar**

```java
<ns1:getAllCompaniesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeExpired>false</ns1:includeExpired>
</ns1:getAllCompaniesParam>
```

**Respuesta**

```java
<ns1:getAllCompaniesReturnxmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyArray>
      <ns1:items>
         <ns1:companyHandle>18</ns1:companyHandle>
         <ns1:name>00webload</ns1:name>
         <ns1:rootPath>00webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.667Z</ns1:expires>
      </ns1:items>
      <ns1:items>
         <ns1:companyHandle>19</ns1:companyHandle>
         <ns1:name>01webload</ns1:name>
         <ns1:rootPath>01webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.414Z</ns1:expires>
      </ns1:items>
      . . .
   </ns1:companyArray>
</ns1:getAllCompaniesReturn>
```

