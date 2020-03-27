---
description: Devuelve grupos de compañías.
seo-description: Devuelve grupos de compañías.
seo-title: getGroups
solution: Experience Manager
title: getGroups
topic: Scene7 Image Production System API
uuid: d6e1542d-83a2-4b25-a986-2465e9e5a145
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

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
| ` *`companyHandle`*` | `xsd:string` | Sí | El identificador de la compañía. |

**Salida (getGroupsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`groupArray`*` | `types:GroupArray` | Sí | Matriz de grupos. |

## Ejemplos {#section-ed0708f611574354bf0c6ea83912b531}

Este código devuelve una matriz que contiene todos los grupos que pertenecen a una compañía específica e información específica sobre cada grupo.

**Solicitar**

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

