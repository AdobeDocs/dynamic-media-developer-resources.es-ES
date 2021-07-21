---
description: Recursos que pertenecen a un conjunto de imágenes.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Conjuntos de imágenes
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 6%

---

# ImageSetMember{#imagesetmember}

Recursos que pertenecen a un conjunto de imágenes.

Restablecimiento de página significa que un [!DNL eCatalog] debe iniciar una página nueva. `RenderSet` indica que forma parte de una  `RenderSet` muestra. Se fuerza el valor `true` para los conjuntos `eCatalog` y `RenderSet`.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`asset`*` | `type:Asset` | Recursos en la matriz de conjuntos de imágenes. |
| `*`pageReset`*` | `xsd:boolean` | Inicia una página nueva. Se ignora la configuración y se fuerza el valor a `true` para los conjuntos `eCatalog` y `RenderSet`. |
