---
description: Actualiza el campo de imagen asociado a un recurso de imagen.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 11%

---

# ImageFieldUpdate{#imagefieldupdate}

Actualiza el campo de imagen asociado a un recurso de imagen.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| assetHandle | `xsd:string` | Identificador de recurso. |
| resolution | `xsd:double` | Resolución de imagen en píxeles por pulgada. |
| anchorX | `xsd:int` | Anclaje de imagen del eje X. |
| anchorY | `xsd:int` | Anclaje de imagen del eje Y. |
| Datos de usuario | `xsd:string` | Valor de `userData` campo de metadatos, que se publica en el campo del catálogo de datos del usuario que sirve la imagen. |
