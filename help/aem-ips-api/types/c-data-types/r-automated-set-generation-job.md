---
description: Agrupe archivos en conjuntos mediante una matriz de lista de controladores de recursos.
seo-description: Agrupe archivos en conjuntos mediante una matriz de lista de controladores de recursos.
seo-title: AutomatedSetGenerationJob
solution: Experience Manager
title: AutomatedSetGenerationJob
uuid: 9c664bde-a731-4d6b-ae6b-c862bda02d4c
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 6%

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

Agrupe archivos en conjuntos mediante una matriz de lista de controladores de recursos.

Sintaxis

## Parámetros {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3">Matriz de controles de recursos que se utiliza para crear el conjunto. <p>De forma predeterminada, 1000 es el número máximo de recursos que puede tener en la matriz. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ruta a la carpeta donde desea guardar los conjuntos. Se guarda en la carpeta raíz de la empresa de forma predeterminada. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Establece un indicador para indicar si los recursos deben publicarse o no. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Matriz de scripts de generación establecidos que se pueden ejecutar en los archivos cargados. Consulte <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Configure una notificación de correo electrónico automatizada para el trabajo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Opciones de configuración de correo electrónico**

El parámetro `emailSetting` incluye las siguientes opciones:

| Opción | Devuelve |
|---|---|
| `All` | Todas las notificaciones de trabajos (errores, advertencias, finalización) al destinatario especificado. |
| `Error` | Errores de trabajo en el destinatario especificado. |
| `ErrorAndWarning` | Errores y advertencias de trabajo al destinatario especificado. |
| `JobCompletion` | Una notificación de finalización de trabajo al destinatario especificado. |
| `None` | El trabajo no envía ninguna notificación de trabajo al destinatario especificado. |

## Ejemplo {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```

