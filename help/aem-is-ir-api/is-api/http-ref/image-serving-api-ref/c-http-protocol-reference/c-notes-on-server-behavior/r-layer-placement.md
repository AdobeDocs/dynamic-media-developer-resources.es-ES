---
description: Las capas se colocan alineando el origen de la capa (origin=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.
solution: Experience Manager
title: Colocación de capas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# Colocación de capas{#layer-placement}

Las capas se colocan alineando el origen de la capa (origin=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.

Si el origen de la capa no se especifica explícitamente para una capa de imagen, se calcula de la siguiente manera:

1. Determine el anclaje de la imagen. Utilice `anchor=` o, si no se especifica, `catalog::Anchor`.
1. Si el anclaje de imagen está definido, aplique las transformaciones de capa y `extend=` para convertirla en un valor origin=.
1. Si no se define ningún anclaje de imagen, el origen de la capa se coloca en el centro del rectángulo de la capa (después de aplicar `extend=`).

![](assets/layerplacement.png)

