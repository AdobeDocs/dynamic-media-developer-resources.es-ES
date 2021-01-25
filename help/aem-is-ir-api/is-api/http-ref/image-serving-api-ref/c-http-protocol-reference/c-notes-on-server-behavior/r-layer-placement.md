---
description: Las capas se colocan alineando el origen de la capa (origen=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.
seo-description: Las capas se colocan alineando el origen de la capa (origen=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.
seo-title: Colocación de capas
solution: Experience Manager
title: Colocación de capas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# Colocación de capas{#layer-placement}

Las capas se colocan alineando el origen de la capa (origen=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.

Si el origen de capa no se especifica explícitamente para una capa de imagen, se calcula de la siguiente manera:

1. Determine el anclaje de imagen. Utilice `anchor=` o, si no se especifica, `catalog::Anchor`.
1. Si el anclaje de imagen está definido, aplique las transformaciones de la capa y `extend=` para convertirla en un valor origen=.
1. Si no se define ningún anclaje de imagen, el origen de la capa se coloca en el centro del rectángulo de la capa (después de aplicar `extend=`).

![](assets/layerplacement.png)

