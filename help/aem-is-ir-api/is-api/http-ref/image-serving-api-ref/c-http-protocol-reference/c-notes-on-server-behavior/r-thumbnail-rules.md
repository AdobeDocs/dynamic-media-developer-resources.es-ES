---
description: Tenga en cuenta estas reglas de miniaturas.
solution: Experience Manager
title: Reglas de miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Reglas de miniaturas{#thumbnail-rules}

Tenga en cuenta estas reglas de miniaturas.

1. Si es `catalog::ThumbType=Crop`, la imagen (recortada) se escala al tamaño más pequeño posible mientras cubre todo el recto de destino. Si es `catalog::ThumbType=Fit`, la imagen (recortada) se escala al tamaño más grande posible y, al mismo tiempo, se sigue ajustando toda la imagen al rectángulo de destino. Si es `catalog::ThumbType=Texture`, la imagen (recortada) se escala a la proporción de `catalog::ThumbRes` a `catalog::Resolution`.
1. Alinee la imagen escalada con el recto de destino en función de `attribute::ThumbHorizAlign` y `attribute::ThumbVertAlign`.
1. Recorte el resultado hasta el recto de destino.
