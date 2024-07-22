---
description: El registro de trabajo después de ejecutar el trabajo.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# [!DNL JobLog]{#joblog}

El registro de trabajo después de ejecutar el trabajo.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| companyHandle | `xsd:string` | Manejo de la compañía. |
| jobHandle | `xsd:string` | Gestor del trabajo. |
| jobName | `xsd:string` | Nombre de trabajo. |
| originalJobName | `xsd:string` | El nombre original enviado para el trabajo con `submitJob`. |
| submitUserEmail | `xsd:string` | La dirección de correo electrónico del usuario que envió el trabajo. |
| logType | `xsd:string` | Elección de los tipos de registro de trabajo. |
| jobSubType | `xsd:string` | Información adicional del trabajo. |
| startDate | `xsd:dateTime` | La fecha, hora y zona horaria de inicio del trabajo. |
| endDate | `xsd:dateTime` | La fecha de finalización, la hora y la zona horaria del trabajo. |
| [!DNL description] | `xsd:string` | Una descripción del trabajo tal como se especificó originalmente en `submitJob`. |
| fileSuccessCount | `xsd:int` | Número de archivos procesados correctamente. |
| fileErrorCount | `xsd:int` | Número de archivos que han causado un error. |
| fileWarningCount | `xsd:int` | Número de archivos que generaron una advertencia. |
| fileDuplicateCount | `xsd:int` | Número de archivos duplicados. |
| fileUpdateCount | `xsd:int` | Número de archivos actualizados. |
| totalFileCount | `xsd:int` | Número de archivos procesados por el trabajo registrado. |
| transferSuccessCount | `xsd:int` | Número de transferencias correctas. |
| transferErrorCount | `xsd:int` | Número de errores de transferencia. |
| transferWarningCount | `xsd:int` | Número de advertencias de transferencia. |
| fatalError | `xsd:boolean` | Si el trabajo ha generado un error grave. |
| detailTotalRows | `xsd:int` | Número total de filas que coinciden con la consulta, que puede ser mayor que el tamaño de `detailArray` debido a los límites de tamaño de página. |
| detailArray | `types:JobLogDetailArray` | La matriz de detalles sobre el trabajo registrado. |
