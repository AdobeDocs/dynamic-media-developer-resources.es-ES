---
description: Obtiene los registros de trabajo especificados para la empresa seleccionada. Puede ordenar por caracteres, dirección, fechas de inicio y finalización y número de filas.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
TQID: 'https://experienceleague.adobe.com/lerbQ3ibPCI3zqkrmgPrwTAYp1w6dWxIWYRt2Ij51oA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 10%

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

**Solicitud**

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
