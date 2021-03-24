---
description: Crea un nuevo proyecto.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 18%

---


# createProject{#createproject}

Crea un nuevo proyecto.

Sintaxis

## Tipos de usuarios autorizados {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-8c741884eb54489bbaad0c444fee80b6}

**Entrada (createProjectParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa asociada al nuevo proyecto. |
| `*`projectName`*` | `xsd:string` | Sí | Nuevo nombre del proyecto. |

**Salida (createProjectParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Sí | El identificador del nuevo proyecto. |

## Ejemplos {#section-a0cd532b67e346d088fbec141231a0e5}

Este ejemplo de código crea un proyecto llamado `ApiTestProject` en una empresa especificada por su identificador. La respuesta devuelve el identificador al proyecto.

**Solicitar**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```

