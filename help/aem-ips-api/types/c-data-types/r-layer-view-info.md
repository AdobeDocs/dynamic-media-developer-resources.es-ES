---
description: Propiedades de la vista de capas.
seo-description: Propiedades de la vista de capas.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 10%

---


# LayerViewInfo{#layerviewinfo}

Propiedades de la vista de capas.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`url`*` | `xsd:string` | URL del servidor de imágenes que representa la plantilla. Combina los campos `urlModifier` y `urlPostAp- plyModifier`. |
| `*`urlModifier`*` | `xsd:string` | Comandos de protocolo de servicio de imágenes que se aplican antes de los comandos request o `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Comandos de protocolo de servicio de imágenes para aplicar después de `urlModifier` y comandos de solicitud. |

