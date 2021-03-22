---
description: Cambia el nombre de un proyecto.
seo-description: Cambia el nombre de un proyecto.
seo-title: changeProject
solution: Experience Manager
title: changeProject
uuid: 6303c493-a6fe-4b32-80c3-947aba4190f7
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 20%

---


# changeProject{#renameproject}

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

**Entrada (cambiar nombre de ProjectParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Sí | Gestione a la empresa con el proyecto cuyo nombre desea cambiar. |
| `*`projectHandle`*` | `xsd:string` | Sí | Gestione el proyecto. |
| `*`projectName`*` | `xsd:string` | Sí | Nuevo nombre del proyecto. |

**Salida (filenameProjectParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Sí | Identificador del proyecto cuyo nombre ha cambiado. |

## Ejemplos {#section-a0a06d9244774795b695a10b92b2a5e7}

Este ejemplo de código cambia el nombre de un proyecto y devuelve el identificador del proyecto.

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

