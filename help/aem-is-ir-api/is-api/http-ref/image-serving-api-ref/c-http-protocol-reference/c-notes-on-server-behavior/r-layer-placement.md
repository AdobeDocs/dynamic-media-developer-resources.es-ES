---
title: Colocación de capas
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Colocación de capas{#layer-placement}

Las capas se colocan alineando el origen de la capa (origin=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.

Si el origen de la capa no se especifica explícitamente para una capa de imagen, se calcula de la siguiente manera:

1. Determine el anclaje de la imagen. Utilice `anchor=` o, si no se especifica, `catalog::Anchor`.
1. Si el anclaje de imagen está definido, aplique las transformaciones de capa y `extend=` para convertirla en un valor origin=.
1. Si no se define ningún anclaje de imagen, el origen de la capa se coloca en el centro del rectángulo de la capa (después de aplicar `extend=`).

![Imagen de colocación de capa](assets/layerplacement.png)
