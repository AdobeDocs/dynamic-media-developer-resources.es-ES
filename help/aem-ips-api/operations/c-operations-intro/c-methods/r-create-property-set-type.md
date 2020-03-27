---
description: Un tipo de conjunto de propiedades especifica varias opciones de configuración utilizadas para administrar conjuntos de propiedades.
seo-description: Un tipo de conjunto de propiedades especifica varias opciones de configuración utilizadas para administrar conjuntos de propiedades.
seo-title: createPropertySetType
solution: Experience Manager
title: createPropertySetType
topic: Scene7 Image Production System API
uuid: ecbaad48-d725-4f7a-a37d-5e4cde3295cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createPropertySetType{#createpropertysettype}

Un tipo de conjunto de propiedades especifica varias opciones de configuración utilizadas para administrar conjuntos de propiedades.

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
| ` *`companyHandle`*` | `xsd:string` | No | El identificador de la compañía que posee el tipo de conjunto de propiedades. Si no `companyHandle` se pasa y el llamador es un `IpsAdmin`, se creará un tipo de conjunto de propiedades globales. |
| ` *`name`*` | `xsd:string` | Sí | Nombre del tipo de conjunto de propiedades. |
| ` *`propertyType`*` | `xsd:string` | Sí | Elección de tipos de conjuntos de propiedades. |
| ` *`allowMultiple`*` | `xsd:boolean` | Sí | Determina si el programa puede tener varios conjuntos de propiedades. |

**Output (createPropertySetTypeReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | Sí | Un identificador para el tipo. |

## Ejemplos {#section-13396c9639a6475190e622eae3cdb534}

Este ejemplo de código crea un conjunto de propiedades con un nombre y un tipo especificados por la `PropertySet Types` constante. El identificador de la compañía que posee el tipo de conjunto de propiedades. Si companyHandle no se pasa y el llamador es un IpsAdmin, se creará un tipo de conjunto de propiedades globales.

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

