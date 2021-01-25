---
description: Cambia el nombre de un proyecto.
seo-description: Cambia el nombre de un proyecto.
seo-title: RenameProject
solution: Experience Manager
title: RenameProject
topic: Dynamic Media Image Production System API
uuid: 6303c493-a6fe-4b32-80c3-947aba4190f7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 22%

---


# RenameProject{#renameproject}

Cambia el nombre de un proyecto.

Sintaxis

## Tipos de usuarios autorizados {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-43ccd77648784be4a259a723c3e1db40}

**Entrada (cambiar el nombre de ProjectParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Sí | Administre la compañía con el proyecto cuyo nombre desee cambiar. |
| `*`projectHandle`*` | `xsd:string` | Sí | Gestionar el proyecto. |
| `*`projectName`*` | `xsd:string` | Sí | Nuevo nombre de proyecto. |

**Salida (cambiar el nombre de ProjectParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Sí | Identificador del proyecto cuyo nombre se ha cambiado. |

## Ejemplos {#section-a0a06d9244774795b695a10b92b2a5e7}

Este ejemplo de código cambia el nombre de un proyecto y devuelve el control del proyecto.

**Solicitar**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**Respuesta**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```

