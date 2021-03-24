---
description: El registro de trabajos después de que se haya ejecutado el trabajo.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 3%

---


# JobLog{#joblog}

El registro de trabajos después de que se haya ejecutado el trabajo.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Identificador de la empresa. |
| `*`jobHandle`*` | `xsd:string` | Identificador de trabajo. |
| `*`jobName`*` | `xsd:string` | Nombre de trabajo. |
| `*`originalJobName`*` | `xsd:string` | El nombre original enviado para el trabajo con `submitJob`. |
| `*`submitUserEmail`*` | `xsd:string` | La dirección de correo electrónico del usuario que envió el trabajo. |
| `*`logType`*` | `xsd:string` | Elección de tipos de registro de trabajos. |
| `*`jobSubType`*` | `xsd:string` | Información adicional del trabajo. |
| `*`startDate`*` | `xsd:dateTime` | La fecha de inicio, la hora y la zona horaria del trabajo. |
| `*`endDate`*` | `xsd:dateTime` | Fecha, hora y zona horaria de finalización del trabajo. |
| `*`descripción`*` | `xsd:string` | Descripción del trabajo tal como se especificó originalmente en `submitJob`. |
| `*`fileSuccessCount`*` | `xsd:int` | Número de archivos procesados correctamente. |
| `*`fileErrorCount`*` | `xsd:int` | Número de archivos que provocaron un error. |
| `*`fileWarningCount`*` | `xsd:int` | Número de archivos que generaron una advertencia. |
| `*`fileDuplicateCount`*` | `xsd:int` | Número de archivos duplicados. |
| `*`fileUpdateCount`*` | `xsd:int` | Número de archivos actualizados. |
| `*`totalFileCount`*` | `xsd:int` | Número de archivos procesados por el trabajo registrado. |
| `*`transferSuccessCount`*` | `xsd:int` | Número de transferencias correctas. |
| `*`transferErrorCount`*` | `xsd:int` | Número de errores de transferencia. |
| `*`transferWarningCount`*` | `xsd:int` | Número de advertencias de transferencia. |
| `*`mortalError`*` | `xsd:boolean` | Si el trabajo generó un error grave. |
| `*`detailTotalRows`*` | `xsd:int` | El número total de filas que coinciden con la consulta, que puede ser mayor que el tamaño de `detailArray` debido a los límites de tamaño de página. |
| `*`detailArray`*` | `types:JobLogDetailArray` | Matriz de detalles sobre el trabajo registrado. |

