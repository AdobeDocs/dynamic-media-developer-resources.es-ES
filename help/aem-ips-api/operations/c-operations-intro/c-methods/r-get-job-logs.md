---
description: Obtiene los registros de trabajo especificados para la compañía seleccionada. Puede ordenar por caracteres, dirección, fechas de inicio y finalización y número de filas.
seo-description: Obtiene los registros de trabajo especificados para la compañía seleccionada. Puede ordenar por caracteres, dirección, fechas de inicio y finalización y número de filas.
seo-title: getJobLogs
solution: Experience Manager
title: getJobLogs
topic: Scene7 Image Production System API
uuid: 850ccfad-6cdb-4eda-a20a-762fadadf8b2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 10%

---


# getJobLogs{#getjoblogs}

Obtiene los registros de trabajo especificados para la compañía seleccionada. Puede ordenar por caracteres, dirección, fechas de inicio y finalización y número de filas.

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

**Input (getJobLogsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | No | El identificador de compañía. |
| ` *`userHandle`*` | `xsd:string` | No | Obtiene registros de trabajos enviados por un usuario específico. |
| ` *`sortBy`*` | `xsd:string` | No | Permite seleccionar campos de ordenación. |
| ` *`sortDirection`*` | `xsd:string` | No | Orden (ascendente o descendente). |
| ` *`startDate`*` | `xsd:dateTime` | No | Fecha y hora del inicio del registro de trabajos. Proporcione el huso horario con la solicitud para este campo. |
| ` *`endDate`*` | `xsd:dateTime` | No | Fecha y hora del final del registro de trabajos. Proporcione el huso horario con la solicitud para este campo. |
| ` *`numRows`*` | `xsd:int` | No | Número máximo de filas que devolver. |

**Salida (getJobLogsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`jobLogArray`*` | `types: JobLogArray` | Sí | Matriz de registros de trabajos. |

## Ejemplos {#section-35871c94b4a44559912577efddbc46a6}

Este ejemplo de código devuelve registros de trabajo IPS para una compañía específica. También puede utilizarla para devolver registros de trabajo para un usuario o compañía y usuario específicos.

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

