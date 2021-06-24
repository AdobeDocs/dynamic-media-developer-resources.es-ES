---
description: Gestiona los derechos para acceder, modificar, crear o eliminar recursos por grupo.
solution: Experience Manager
title: Permiso
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
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
