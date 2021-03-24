---
description: Devuelve 2 tipos diferentes de información en función de los parámetros transferidos. originatorHandle devuelve información sobre los recursos generados a partir del recurso especificado. generateHandle devuelve información sobre los pasos utilizados para generar el recurso o archivo especificado.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 9%

---


# getGenerationInfo{#getgenerationinfo}

Devuelve 2 tipos diferentes de información en función de los parámetros transferidos. originatorHandle devuelve información sobre los recursos generados a partir del recurso especificado. generateHandle devuelve información sobre los pasos utilizados para generar el recurso o archivo especificado.

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
| `*`Frase de código`*` | `xsd:string` | Sí | El identificador de la empresa. |
| `*`Frase de código`*` | `xsd:string` | No | Motor utilizado en la generación. Consulte Estilos de fuente. |
| `*`Frase de código`*` | `xsd:string` | No | El controlador del recurso que se va a consultar para los recursos generados. |
| `*`Frase de código`*` | `xsd:string` | No | El controlador del recurso que se va a consultar para los recursos y motores utilizados en su generación. |
| `*`Frase de código`*` | `xsd:StringArray` | No | Propiedades incluidas en la operación. |
| `*`Frase de código`*` | `xsd:StringArray` | No | Propiedades excluidas de la operación. |

**Salida (getGenerationInfoReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`generationArray`*` | `types:GenerationInfoArray` | Sí | Matriz de información de generación. |

## Ejemplos {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Este ejemplo de código devuelve información sobre los recursos generados a partir de un recurso específico. No recupera información sobre los pasos utilizados para generar el recurso especificado. La respuesta se trunca para su brevedad.

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

