---
description: Tenga en cuenta estas reglas de miniaturas.
seo-description: Tenga en cuenta estas reglas de miniaturas.
seo-title: Reglas de miniaturas
solution: Experience Manager
title: Reglas de miniaturas
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# Reglas de miniatura{#thumbnail-rules}

Tenga en cuenta estas reglas de miniaturas.

1. Si es `catalog::ThumbType=Crop`, la imagen (recortada) se escala al tamaño más pequeño posible mientras cubre todo el recto de destino. Si es `catalog::ThumbType=Fit`, la imagen (recortada) se escala al tamaño más grande posible y, al mismo tiempo, se sigue ajustando toda la imagen al rectángulo de destino. Si es `catalog::ThumbType=Texture`, la imagen (recortada) se escala a la proporción de `catalog::ThumbRes` a `catalog::Resolution`.
1. Alinee la imagen escalada con el recto de destino en función de `attribute::ThumbHorizAlign` y `attribute::ThumbVertAlign`.
1. Recorte el resultado hasta el recto de destino.

