---
description: Agrega una empresa al sistema.
solution: Experience Manager
title: addCompany
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 12%

---


# addCompany{#addcompany}

Agrega una empresa al sistema.

Envía el nombre de la empresa que se agregará al sistema y, opcionalmente, envía si la empresa caduca.

Cuando se invoca esta operación, el sistema obtiene un tipo `*`companyInfo`*` que contiene un identificador de empresa y campos descriptivos. Si el nombre de empresa solicitado ya existe en el sistema, genera un `ipsApiFault`.

## Tipos de usuarios autorizados {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-c64a21b72585447880760db9e7a12ccb}

**Entrada (addCompanyParam)**

<table id="table_AA915BAD2E8E4A1B9719725994309CE8"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Nombre de la empresa que se va a agregar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> expires</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:dateTime</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>La fecha de caducidad de la empresa. Proporcione la zona horaria con la solicitud para este campo. Las zonas horarias se ajustan a la hora central. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (addCompanyReturn)**

<table id="table_89EBAC0E0FB34793BD843837BB02B518"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Gestione y nombre, ruta raíz, fecha de caducidad y hora de la nueva empresa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplos {#section-4c8f1bb40d154c77a7b410468206e52b}

En este ejemplo se muestra una solicitud para agregar una empresa al sistema IPS y la respuesta que detalla la información sobre la empresa agregada necesaria para realizar otras operaciones.

**Solicitar**

```java
<ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:addCompanyParam>
```

**Respuesta**

```java
<ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:addCompanyReturn>
```

