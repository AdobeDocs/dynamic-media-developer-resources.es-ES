---
description: Recursos que pertenecen a un conjunto de imágenes.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Conjuntos de imágenes
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
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

