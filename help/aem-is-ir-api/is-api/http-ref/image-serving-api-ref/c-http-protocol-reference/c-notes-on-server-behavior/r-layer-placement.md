---
description: Las capas se colocan alineando el origen de la capa (origin=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.
seo-description: Las capas se colocan alineando el origen de la capa (origin=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.
seo-title: Colocación de capas
solution: Experience Manager
title: Colocación de capas
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Colocación de capas{#layer-placement}

Las capas se colocan alineando el origen de la capa (origin=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.

Si el origen de la capa no se especifica explícitamente para una capa de imagen, se calcula de la siguiente manera:

1. Determine el anclaje de la imagen. Utilice `anchor=` o, si no se especifica, `catalog::Anchor`.
1. Si el anclaje de imagen está definido, aplique las transformaciones de capa y `extend=` para convertirla en un valor origin=.
1. Si no se define ningún anclaje de imagen, el origen de la capa se coloca en el centro del rectángulo de la capa (después de aplicar `extend=`).

![](assets/layerplacement.png)

