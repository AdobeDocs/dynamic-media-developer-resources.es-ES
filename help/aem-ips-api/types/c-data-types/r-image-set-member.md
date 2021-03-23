---
description: Recursos que pertenecen a un conjunto de imágenes.
seo-description: Recursos que pertenecen a un conjunto de imágenes.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
feature: Dynamic Media Classic,SDK/API,Conjuntos de imágenes
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---


# ImageSetMember{#imagesetmember}

Recursos que pertenecen a un conjunto de imágenes.

Restablecimiento de página significa que un [!DNL eCatalog] debe iniciar una página nueva. `RenderSet` indica que forma parte de una  `RenderSet` muestra. Se fuerza el valor `true` para los conjuntos `eCatalog` y `RenderSet`.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`asset`*` | `type:Asset` | Recursos en la matriz de conjuntos de imágenes. |
| `*`pageReset`*` | `xsd:boolean` | Inicia una página nueva. Se ignora la configuración y se fuerza el valor a `true` para los conjuntos `eCatalog` y `RenderSet`. |

