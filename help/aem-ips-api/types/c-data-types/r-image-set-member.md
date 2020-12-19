---
description: Recursos que pertenecen a un conjunto de imágenes.
seo-description: Recursos que pertenecen a un conjunto de imágenes.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Scene7 Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 6%

---


# ImageSetMember{#imagesetmember}

Recursos que pertenecen a un conjunto de imágenes.

El restablecimiento de página significa que un [!DNL eCatalog] debe inicio de una nueva página. `RenderSet` indica que forma parte de una  `RenderSet` muestra. El valor se fuerza a `true` para `eCatalog` y `RenderSet` conjuntos.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`asset`*` | `type:Asset` | Recursos de la matriz de conjuntos de imágenes. |
| ` *`pageReset`*` | `xsd:boolean` | Inicio una página nueva. Se omite la configuración y se fuerza el valor a `true` para `eCatalog` y `RenderSet` conjuntos. |

