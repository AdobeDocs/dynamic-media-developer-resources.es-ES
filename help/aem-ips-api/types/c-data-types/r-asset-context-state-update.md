---
title: AssetContextStateUpdate
description: Establezca un nuevo conjunto de indicadores de estado de publicación para el contexto de publicación asociado a un recurso.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 6%

---

# AssetContextStateUpdate{#assetcontextstateupdate}

Establezca un nuevo conjunto de indicadores de estado de publicación para el contexto de publicación asociado a un recurso.

**Parámetros**

| Nombre | Tipo | Descripción |
|---|---|---|
| assetHandle | `xsd:string` | Gestione el recurso que desea actualizar. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | Matriz de estados de contacto de publicación para el recurso que desea actualizar. |
