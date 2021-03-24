---
description: Tenga en cuenta estas reglas de miniaturas.
solution: Experience Manager
title: Reglas de miniaturas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Reglas de miniatura{#thumbnail-rules}

Tenga en cuenta estas reglas de miniaturas.

1. Si es `catalog::ThumbType=Crop`, la imagen (recortada) se escala al tamaño más pequeño posible mientras cubre todo el recto de destino. Si es `catalog::ThumbType=Fit`, la imagen (recortada) se escala al tamaño más grande posible y, al mismo tiempo, se sigue ajustando toda la imagen al rectángulo de destino. Si es `catalog::ThumbType=Texture`, la imagen (recortada) se escala a la proporción de `catalog::ThumbRes` a `catalog::Resolution`.
1. Alinee la imagen escalada con el recto de destino en función de `attribute::ThumbHorizAlign` y `attribute::ThumbVertAlign`.
1. Recorte el resultado hasta el recto de destino.

