---
description: Devuelve grupos de compañías.
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 21%

---

# getGroups{#getgroups}

Devuelve grupos de compañías.

Sintaxis

## Tipos de usuarios autorizados {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-0e06195f23dd4c69922df210f566dd18}

**Entrada (getGroupsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía. |

**Salida (getGroupsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| groupArray | `types:GroupArray` | Sí | Matriz de grupos. |

## Ejemplos {#section-ed0708f611574354bf0c6ea83912b531}

Este código devuelve una matriz que contiene todos los grupos que pertenecen a una compañía específica e información específica sobre cada grupo.

**Solicitud**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```
