---
description: Devuelve información sobre la compañía especificada, incluido el identificador de la compañía, el nombre de la compañía, la ruta de acceso raíz y la fecha de caducidad. Debe especificar companyHandle o companyName cuya información desea recuperar.
solution: Experience Manager
title: getCompanyInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72bd223b-c99a-48a3-9c0a-d1af392d904c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 7%

---

# getCompanyInfo{#getcompanyinfo}

Devuelve información sobre la compañía especificada, incluido el identificador de la compañía, el nombre de la compañía, la ruta de acceso raíz y la fecha de caducidad. Debe especificar companyHandle o companyName cuya información desea recuperar.

Sintaxis

## Tipos de usuarios autorizados {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-7dec8871c89a414c9f066adade1831d8}

**Entrada (getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Se requiere <span class="codeph"> <span class="varname"> companyHandle</span> </span> o <span class="codeph"> <span class="varname"> companyName</span> </span>. </p> </td> 
   <td colname="col4"> <p>El identificador de la compañía cuya información desea obtener. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Se requiere <span class="codeph"> <span class="varname"> companyHandle</span> </span> o <span class="codeph"> <span class="varname"> companyName</span> </span>. </p> </td> 
   <td colname="col4"> <p>El nombre de la compañía cuya información desea obtener. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> informaciónDeEmpresa</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:Empresa</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Información descriptiva sobre la empresa y del identificador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplos {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

Este ejemplo de código devuelve toda la información sobre una compañía utilizando un nombre de compañía y un identificador. Devuelve datos similares a la respuesta recibida al crear una empresa.

**Solicitud**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**Respuesta**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```
