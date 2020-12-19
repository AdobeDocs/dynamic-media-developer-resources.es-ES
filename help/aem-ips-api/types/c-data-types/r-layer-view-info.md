---
description: Propiedades de vista de capas.
seo-description: Propiedades de vista de capas.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Scene7 Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# LayerViewInfo{#layerviewinfo}

Propiedades de vista de capas.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`url`*` | `xsd:string` | URL del servidor de imágenes que representa la plantilla. Combina campos `urlModifier` y `urlPostAp- plyModifier`. |
| ` *`urlModifier`*` | `xsd:string` | Comandos de protocolo de servicio de imágenes para aplicar antes de los comandos request o `urlPostApplyModifier`. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Comandos de protocolo de servicio de imágenes para aplicar después de `urlModifier` y comandos de solicitud. |

