---
description: Tenga en cuenta estas reglas para las miniaturas.
solution: Experience Manager
title: Reglas de miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# Reglas de miniaturas{#thumbnail-rules}

Tenga en cuenta estas reglas para las miniaturas.

1. If `catalog::ThumbType=Crop`A continuación, la imagen (recortada) se escala al tamaño más pequeño posible mientras sigue cubriendo toda la recta de destino. If `catalog::ThumbType=Fit`A continuación, la imagen (recortada) se escala al mayor tamaño posible sin dejar de encajar toda la imagen en la parte recta de destino. If `catalog::ThumbType=Texture`, la imagen (recortada) se escala a la proporción de `catalog::ThumbRes` hasta `catalog::Resolution`.
1. Alinee la imagen a escala con la recta de destino basándose en `attribute::ThumbHorizAlign` y `attribute::ThumbVertAlign`.
1. Recorte el resultado en la dirección correcta de destino.
