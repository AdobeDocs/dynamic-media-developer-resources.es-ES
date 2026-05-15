---
description: Un tipo de conjunto de propiedades especifica varios valores utilizados para ayudar a administrar los conjuntos de propiedades.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
TQID: 'https://experienceleague.adobe.com/JOAxK9j-P0v8inQRU65C2rVCM9-OnXTXCF6wtp6eksY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 10%

---

# createPropertySetType{#createpropertysettype}

Un tipo de conjunto de propiedades especifica varios valores utilizados para ayudar a administrar los conjuntos de propiedades.

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
| companyHandle | `xsd:string` | No | El identificador de la compañía propietaria del tipo de conjunto de propiedades. Si no se pasa `companyHandle` y el llamador es un `IpsAdmin`, se crea un tipo de conjunto de propiedades global. |
| nombre | `xsd:string` | Sí | Nombre del tipo del conjunto de propiedades. |
| propertyType | `xsd:string` | Sí | Elección de tipos de conjuntos de propiedades. |
| allowMultiple | `xsd:boolean` | Sí | Determina si el programa puede tener varios conjuntos de propiedades. |

**Salida (createPropertySetTypeReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| typeHandle | `xsd:string` | Sí | Un identificador para el tipo. |

## Ejemplos {#section-13396c9639a6475190e622eae3cdb534}

Este ejemplo de código crea un conjunto de propiedades con un nombre y un tipo especificados por la constante `PropertySet Types`. El identificador de la compañía propietaria del tipo de conjunto de propiedades. Si companyHandle no se pasa y el llamador es un IpsAdmin, se crea un tipo de conjunto de propiedades global.

**Solicitud**

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
