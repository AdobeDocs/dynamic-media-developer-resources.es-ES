---
description: Assets que pertenecen a un conjunto de imágenes.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

Assets que pertenecen a un conjunto de imágenes.

Restablecer página significa que un [!DNL eCatalog] debe iniciar una nueva página. `RenderSet` indica que forma parte de una muestra `RenderSet`. Se forzó el valor a `true` para `eCatalog` y `RenderSet` conjuntos.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| asset | `type:Asset` | Assets en la matriz del conjunto de imágenes. |
| pageReset | `xsd:boolean` | Inicia una nueva página. Se omite la configuración y se fuerza el valor en `true` para `eCatalog` y `RenderSet` conjuntos. |
