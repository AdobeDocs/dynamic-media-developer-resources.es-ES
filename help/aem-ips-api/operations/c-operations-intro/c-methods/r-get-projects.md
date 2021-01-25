---
description: Obtiene proyectos para un grupo de recursos relacionados.
seo-description: Obtiene proyectos para un grupo de recursos relacionados.
seo-title: getProjects
solution: Experience Manager
title: getProjects
topic: Dynamic Media Image Production System API
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---


# getProjects{#getprojects}

Obtiene proyectos para un grupo de recursos relacionados.

Sintaxis

## Tipos de usuarios autorizados {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-8d549237b8c440b4872a0a086ddc00a1}

**Input (getProjectsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la compañía. |

**Salida (getProjectsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`projectArray`*` | `types:ProjectArray` | Sí | Matriz de proyectos asociados a la compañía. |

## Ejemplos {#section-8b12d0b948f644f68bf9a16060d3849a}

Este ejemplo de código devuelve todos los controladores de proyecto de una matriz de proyectos.

**Solicitar**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**Respuesta**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```

