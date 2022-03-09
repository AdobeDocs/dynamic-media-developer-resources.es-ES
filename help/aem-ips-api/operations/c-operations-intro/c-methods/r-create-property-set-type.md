---
description: Un tipo de conjunto de propiedades especifica varias configuraciones utilizadas para ayudar a administrar conjuntos de propiedades.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 12%

---

# createPropertySetType{#createpropertysettype}

Un tipo de conjunto de propiedades especifica varias configuraciones utilizadas para ayudar a administrar conjuntos de propiedades.

Sintaxis

## Tipos de usuarios autorizados {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-43dece72eb9f44df80f4a119dd2c008b}

**Entrada (createPropertySetTypeParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | No | El identificador de la empresa propietaria del tipo de conjunto de propiedades. If `companyHandle` no se pasa y el llamador es un `IpsAdmin`, se crea un tipo de conjunto de propiedades globales. |
| name | `xsd:string` | Sí | Nombre del tipo de conjunto de propiedades. |
| propertyType | `xsd:string` | Sí | Elección de tipos de conjuntos de propiedades. |
| allowMultiple | `xsd:boolean` | Sí | Determina si el programa puede tener varios conjuntos de propiedades. |

**Salida (createPropertySetTypeReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| typeHandle | `xsd:string` | Sí | Un identificador para el tipo . |

## Ejemplos {#section-13396c9639a6475190e622eae3cdb534}

Este ejemplo de código crea un conjunto de propiedades con un nombre y un tipo especificados por el `PropertySet Types` constante. El identificador de la empresa propietaria del tipo de conjunto de propiedades. Si companyHandle no se pasa y la persona que realiza la llamada es un IpsAdmin, se crea un tipo de conjunto de propiedades globales.

**Solicitar**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**Respuesta**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```
