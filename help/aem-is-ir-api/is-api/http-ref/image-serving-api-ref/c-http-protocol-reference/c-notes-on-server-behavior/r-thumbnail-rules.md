---
description: Tenga en cuenta estas reglas de miniaturas.
seo-description: Tenga en cuenta estas reglas de miniaturas.
seo-title: Reglas de miniatura
solution: Experience Manager
title: Reglas de miniatura
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Reglas de miniatura{#thumbnail-rules}

Tenga en cuenta estas reglas de miniaturas.

1. Si `catalog::ThumbType=Crop`, la imagen (recortada) se escala al tamaño más pequeño posible mientras se cubre todo el rectángulo de destinatario. Si es `catalog::ThumbType=Fit`, la imagen (recortada) se escala al tamaño más grande posible y, al mismo tiempo, se ajusta toda la imagen al rectángulo de destinatario. Si `catalog::ThumbType=Texture`, la imagen (recortada) se escala a la proporción de `catalog::ThumbRes` a `catalog::Resolution`.
1. Alinee la imagen escalada con el rectángulo de destinatario en función de `attribute::ThumbHorizAlign` y `attribute::ThumbVertAlign`.
1. Recorte el resultado hasta el rectángulo de destinatario.

