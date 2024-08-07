---
description: Obtiene los registros de trabajo de un recurso. Los elementos devueltos en la matriz contienen información detallada sobre cada entrada en el registro de trabajos de ese recurso. El campo de respuesta logMessage se localiza en función del campo authHeader.
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 88ec5cab-7eb4-48aa-914f-21311593e463
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 8%

---

# getAssetJobLogs{#getassetjoblogs}

Obtiene los registros de trabajo de un recurso. Los elementos devueltos en la matriz contienen información detallada sobre cada entrada en el registro de trabajos de ese recurso. El campo de respuesta logMessage se localiza en función del campo authHeader.

Sintaxis

## Tipos de usuarios autorizados {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-9586617e124b4da4acb6b66b2a9adad8}

**Entrada (getAssetJobLogsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía a la que pertenece el recurso. |
| assetHandle | `xsd:string` | Sí | El identificador del recurso con los registros de trabajo que se van a recuperar. |

**Salida (getAssetJobLogsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| jobLogArray | `types:AssetJobLogArray` | Sí | Matriz de registro de trabajos. |

## Ejemplos {#section-f03d7f3ec5d043d38227f926fb7609f6}

Este ejemplo de código recupera los registros de trabajo de un recurso específico. La respuesta devuelve una matriz de registro de trabajos con información detallada sobre todos los trabajos en los que se utilizó el recurso.

**Solicitud**

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**Respuesta**

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```
