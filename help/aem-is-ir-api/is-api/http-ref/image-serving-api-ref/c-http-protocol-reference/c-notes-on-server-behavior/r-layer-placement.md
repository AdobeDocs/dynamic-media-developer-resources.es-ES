---
description: Las capas se colocan alineando el origen de la capa (origin=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.
solution: Experience Manager
title: Colocación de capas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Colocación de capas{#layer-placement}

Las capas se colocan alineando el origen de la capa (origin=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.

Si el origen de la capa no se especifica explícitamente para una capa de imagen, se calcula de la siguiente manera:

1. Determine el anclaje de la imagen. Utilice `anchor=` o, si no se especifica, `catalog::Anchor`.
1. Si el anclaje de imagen está definido, aplique las transformaciones de capa y `extend=` para convertirla en un valor origin=.
1. Si no se define ningún anclaje de imagen, el origen de la capa se coloca en el centro del rectángulo de la capa (después de aplicar `extend=`).

![](assets/layerplacement.png)
