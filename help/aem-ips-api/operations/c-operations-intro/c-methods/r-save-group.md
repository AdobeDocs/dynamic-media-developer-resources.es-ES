---
description: Cree o edite un grupo.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 22%

---

# saveGroup{#savegroup}

Cree o edite un grupo.

Sintaxis

## Tipos de usuarios autorizados {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-743610e98dd5494baffcbad6401038eb}

**Entrada (saveGroupParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía con el grupo que desea guardar. |
| groupHandle | `xsd:string` | No | El identificador del grupo. |
| nombre | `xsd:string` | Sí | Nombre del grupo. |
| isSystemDefined | `xsd:boolean` | Sí | `false` es el valor predeterminado. |

**Salida (saveGroupReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| groupHandle | `xsd:string` | Sí | Identificador de grupo. |

## Ejemplos {#section-26eee227ff1f4edabb7fa1240b4d9999}

En este ejemplo de código se crea un grupo que pertenece a una compañía específica. Si el grupo ya existe, se guarda con los valores de parámetro especificados.

**Solicitar**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**Respuesta**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```
