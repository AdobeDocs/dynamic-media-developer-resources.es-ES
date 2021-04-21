---
description: Gestiona los derechos para acceder, modificar, crear o eliminar recursos por grupo.
solution: Experience Manager
title: Permiso
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 11%

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
| `*`isAllowed`*` | `xsd:boolean` | Determina si el permiso está permitido. |
| `*`isOverride`*` | `xsd:boolean` | Determina si el permiso anula a otro. |

