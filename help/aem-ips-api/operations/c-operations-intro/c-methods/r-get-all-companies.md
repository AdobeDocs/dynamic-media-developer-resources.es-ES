---
description: Devuelve una matriz de todas las compañías.
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 21%

---

# getAllCompanies{#getallcompanies}

Devuelve una matriz de todas las compañías.

Sintaxis

## Tipos de usuarios autorizados {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## Parámetros {#section-efd74992e6904ebabe7383b577af4fdb}

**Entrada (getAllCompaniesParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| includeExpired | `xsd:boolean` | Sí | Establezca como true para devolver compañías caducadas y no caducadas. |

**Salida (getAllCompaniesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyArray | `types:CompanyArray` | Sí | La matriz de compañías. |

## Ejemplos {#section-3eecf4e6900b41fb92a0e3214791c6b9}

Este ejemplo de código devuelve todas las empresas de IPS de una matriz. Tenga en cuenta que la respuesta de ejemplo se trunca por su brevedad.

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
