---
description: Agrupar archivos en conjuntos mediante una matriz de lista de control de recursos.
seo-description: Agrupar archivos en conjuntos mediante una matriz de lista de control de recursos.
seo-title: AutomatedSetGenerationJob
solution: Experience Manager
title: AutomatedSetGenerationJob
topic: Scene7 Image Production System API
uuid: 9c664bde-a731-4d6b-ae6b-c862bda02d4c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

Agrupar archivos en conjuntos mediante una matriz de lista de control de recursos.

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
   <td colname="col3">Matriz de controladores de recursos utilizados para crear el conjunto. <p>De forma predeterminada, 1000 es el número máximo de recursos que puede tener en la matriz. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ruta a la carpeta en la que desea guardar los conjuntos. Se guarda en la carpeta raíz de la compañía de forma predeterminada. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Define un indicador para indicar si los recursos deben publicarse o no. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Matriz de secuencias de comandos de generación definidas que se pueden ejecutar en los archivos cargados. Consulte <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Configure una notificación de correo electrónico automatizada para el trabajo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**opciones de configuración de correo electrónico**

El parámetro `emailSetting` incluye las siguientes opciones:

| Opción | Devuelve |
|---|---|
| `All` | Todas las notificaciones de trabajo (errores, advertencias, finalización) al destinatario especificado. |
| `Error` | Errores de trabajo en el destinatario especificado. |
| `ErrorAndWarning` | Errores y advertencias de trabajo en el destinatario especificado. |
| `JobCompletion` | Una notificación de finalización de trabajos al destinatario especificado. |
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

