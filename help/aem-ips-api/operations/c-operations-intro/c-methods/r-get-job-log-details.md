---
description: Obtiene los detalles del registro de trabajo de una compañía.
solution: Experience Manager
title: getJobLogDetails
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d2e4eea6-041b-4a80-beda-cbb8d74cd50b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 11%

---

# getJobLogDetails{#getjoblogdetails}

Obtiene los detalles del registro de trabajo de una compañía.

El campo de respuesta `logMessage` está localizado en función del campo `authHeader` `locale`.

## Tipos de usuarios autorizados {#section-6f720a7baad64eb3805868c88af9a960}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-47d411a755224c23a4521f10341d66ab}

**Entrada (getJobLogDetailsParam)**

<table id="table_A77122D73F684B3F8F5AFA1C11C189ED"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obligatorio </th> 
   <th colname="col4" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El identificador de la compañía a la que pertenece el registro de trabajos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Un identificador para un trabajo activo o completado. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Nombre original del registro de trabajos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Una o varias constantes de Tipo de registro. Si está presente, solo se devuelven los tipos de registro especificados. De forma predeterminada, se devuelven todos los tipos de registro. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Número máximo de <span class="codeph"> detailArray</span> elementos que se van a devolver. El valor máximo y predeterminado es 1000. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Número de página de <span class="codeph"> recordsPerPage</span>-results que se van a devolver. El valor predeterminado es 1. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Uno de los valores constantes del campo de ordenación de detalles del trabajo (Date o LogType). El valor predeterminado es Fecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Una de las constantes de cadena Dirección de ordenación. El valor predeterminado es ascendente. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (getJobLogDetailsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| jobLogArray | `types:JobLogArray` | Sí | Matriz de registros de trabajos. |

## Ejemplos {#section-007678b8b8d94e8f91d09f6bc855f394}

Este ejemplo de código devuelve todos los detalles del registro de trabajos de una compañía específica. La primera matriz contiene detalles de registro de trabajos estándar. Una matriz incrustada devuelve información adicional sobre el trabajo.

**Solicitud**

```java
<ns1:getJobLogDetailsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:jobHandle>47||Add_2007-09-14-15:04:34</ns1:jobHandle>
</ns1:getJobLogDetailsParam>
```

**Respuesta**

```java
<getJobLogDetailsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>some_address@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
         <detailArray>
            <items>
               <logMessage>Upload has begun!</logMessage>
               <logType>BeginUpload</logType>
            </items>
            <items>
               <logMessage>Add_2007-09-14-15:04:34</logMessage>
               <logType>OriginalJobName</logType>
            </items>
            <items>
               <logMessage>s7oslo</logMessage>
               <logType>JobClient</logType>
            </items>
            ...
         </detailArray>
      </items>
   </jobLogArray>
</getJobLogDetailsReturn>
```
