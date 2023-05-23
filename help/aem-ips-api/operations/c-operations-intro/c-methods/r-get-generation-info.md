---
description: Devuelve dos tipos diferentes de información en función de los parámetros pasados. originatorHandle devuelve información sobre los recursos generados a partir del recurso especificado. generateHandle devuelve información sobre los pasos utilizados para generar el recurso o archivo especificado.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 10%

---

# getGenerationInfo{#getgenerationinfo}

Devuelve dos tipos diferentes de información en función de los parámetros pasados. originatorHandle devuelve información sobre los recursos generados a partir del recurso especificado. generateHandle devuelve información sobre los pasos utilizados para generar el recurso o archivo especificado.

Sintaxis

## Tipos de usuarios autorizados {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-b7fa94c82147455888e8469fa5f6922b}

**Entrada (getGenerationInfoParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| Frase de código | `xsd:string` | Sí | El identificador de la compañía. |
| Frase de código | `xsd:string` | No | El motor que se utilizó en la generación. Consulte Estilos de fuente. |
| Frase de código | `xsd:string` | No | El identificador del recurso al que consultar los recursos generados. |
| Frase de código | `xsd:string` | No | El identificador del recurso para consultar los recursos y motores utilizados en su generación. |
| Frase de código | `xsd:StringArray` | No | Propiedades incluidas en la operación. |
| Frase de código | `xsd:StringArray` | No | Propiedades excluidas de la operación. |

**Salida (getGenerationInfoReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | Sí | Matriz de información de generación. |

## Ejemplos {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Este ejemplo de código devuelve información sobre los recursos generados a partir de un recurso específico. No recupera información sobre los pasos utilizados para generar el recurso especificado. La respuesta se trunca por su brevedad.

**Solicitar**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**Respuesta**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```
