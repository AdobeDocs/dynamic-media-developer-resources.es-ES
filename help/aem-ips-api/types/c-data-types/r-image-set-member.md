---
description: Recursos que pertenecen a un conjunto de imágenes.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 7%

---

# ImageSetMember{#imagesetmember}

Recursos que pertenecen a un conjunto de imágenes.

Restablecimiento de página significa que [!DNL eCatalog] debe comenzar una página nueva. `RenderSet` indica que forma parte de un `RenderSet` muestra. Se fuerza el valor en `true` para `eCatalog` y `RenderSet` conjuntos.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| asset | `type:Asset` | Recursos en la matriz de conjuntos de imágenes. |
| pageReset | `xsd:boolean` | Inicia una página nueva. Se ignora la configuración y se fuerza el valor en `true` para `eCatalog` y `RenderSet` conjuntos. |
