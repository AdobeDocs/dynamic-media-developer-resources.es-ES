---
description: Propiedades de vista de capa.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 13%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

Propiedades de vista de capa.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| url | `xsd:string` | URL del servidor de imágenes que representa la plantilla. Combina `urlModifier` y `urlPostAp- plyModifier` campos. |
| urlModifier | `xsd:string` | Comandos de protocolo de servicio de imágenes que se aplicarán antes de la solicitud o `urlPostApplyModifier` comandos. |
| urlPostApplyModifier | `xsd:string` | Comandos de protocolo de servicio de imágenes para aplicar después de `urlModifier` y comandos de solicitud. |
