---
description: Tenga en cuenta estas reglas para las miniaturas.
solution: Experience Manager
title: Reglas de miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
TQID: 'https://experienceleague.adobe.com/2HjWzEcMFnTFzwDWz-Ld7wZ6FsFcq3gwaUFcSWgxPko'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# Reglas de miniaturas{#thumbnail-rules}

Tenga en cuenta estas reglas para las miniaturas.

1. Si se usa `catalog::ThumbType=Crop`, la imagen (recortada) se escala al tamaño más pequeño posible mientras se sigue cubriendo todo el recto de destino. Si es `catalog::ThumbType=Fit`, la imagen (recortada) se escala al tamaño más grande posible mientras se sigue ajustando toda la imagen en la dirección de destino. Si `catalog::ThumbType=Texture`, la imagen (recortada) se escala a la proporción de `catalog::ThumbRes` a `catalog::Resolution`.
1. Alinee la imagen a escala con el destino rect basado en `attribute::ThumbHorizAlign` y `attribute::ThumbVertAlign`.
1. Recorte el resultado en la dirección correcta de destino.
