---
title: AssetContextStateUpdate
description: Establezca un nuevo conjunto de indicadores de estado de publicación para el contexto de publicación asociado a un recurso.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

Establezca un nuevo conjunto de indicadores de estado de publicación para el contexto de publicación asociado a un recurso.

**Parámetros**

| Nombre | Tipo | Descripción |
|---|---|---|
| assetHandle | `xsd:string` | Administre al recurso que desea actualizar. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | Una matriz de estados de contacto de publicación para el recurso que desea actualizar. |
