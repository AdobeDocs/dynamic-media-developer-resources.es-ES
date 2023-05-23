---
description: Obtiene los registros de trabajo especificados para la empresa seleccionada. Puede ordenar por caracteres, dirección, fechas de inicio y finalización y número de filas.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 11%

---

# getJobLogs{#getjoblogs}

Obtiene los registros de trabajo especificados para la empresa seleccionada. Puede ordenar por caracteres, dirección, fechas de inicio y finalización y número de filas.

Sintaxis

## Tipos de usuarios autorizados {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-8cfdc7994da24678a45edcb37e9a2166}

**Entrada (getJobLogsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | No | El nombre de la empresa. |
| userHandle | `xsd:string` | No | Obtiene registros para los trabajos enviados por un usuario específico. |
| sortBy | `xsd:string` | No | Permite seleccionar los campos de ordenación. |
| sortDirection | `xsd:string` | No | Orden (ascendente o descendente). |
| startDate | `xsd:dateTime` | No | La fecha y hora de inicio del registro de trabajos. Proporcione la zona horaria con la solicitud para este campo. |
| endDate | `xsd:dateTime` | No | La fecha y hora del final del registro de trabajos. Proporcione la zona horaria con la solicitud para este campo. |
| numRows | `xsd:int` | No | Número máximo de filas que se devolverán. |

**Salida (getJobLogsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | Sí | Matriz de registros de trabajos. |

## Ejemplos {#section-35871c94b4a44559912577efddbc46a6}

Este ejemplo de código devuelve los registros de trabajos de IPS de una compañía específica. También puede utilizarlo para devolver registros de trabajo de un usuario o compañía y usuario específicos.

**Solicitar**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**Respuesta**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```
