---
description: Gestiona los derechos para acceder, modificar, crear o eliminar recursos por grupo.
seo-description: Gestiona los derechos para acceder, modificar, crear o eliminar recursos por grupo.
seo-title: Permiso
solution: Experience Manager
title: Permiso
topic: Dynamic Media Image Production System API
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 10%

---


# Permiso{#permission}

Gestiona los derechos para acceder, modificar, crear o eliminar recursos por grupo.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Identificador de grupo. |
| `*`groupName`*` | `xsd:string` | Nombre del grupo. |
| `*`permissionType`*` | `xsd:string` | Elección del tipo de permiso. |
| `*`isAllowed`*` | `xsd:boolean` | Determina si se permite el permiso. |
| `*`isOverride`*` | `xsd:boolean` | Determina si el permiso anula a otro. |

