---
description: Propiedades de la vista de capas.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 11%

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

