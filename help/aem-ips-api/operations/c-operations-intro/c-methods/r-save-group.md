---
description: Cree o edite un grupo.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 21%

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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con el grupo que desea guardar. |
| `*`groupHandle`*` | `xsd:string` | No | El identificador del grupo. |
| `*`name`*` | `xsd:string` | Sí | Nombre del grupo. |
| `*`isSystemDefined`*` | `xsd:boolean` | Sí | `false` es el valor predeterminado. |

**Salida (saveGroupReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Sí | Identificador de grupo. |

## Ejemplos {#section-26eee227ff1f4edabb7fa1240b4d9999}

Este ejemplo de código crea un grupo que pertenece a una empresa específica. Si el grupo ya existe, se guarda con los valores de parámetro especificados.

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

