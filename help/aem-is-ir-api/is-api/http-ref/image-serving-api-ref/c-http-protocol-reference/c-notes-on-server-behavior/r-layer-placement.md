---
title: Colocación de capas
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
TQID: https://experienceleague.adobe.com/SMf4V0AmxYIi0o0FZhMkRx9pprIxjJjEcCWT2agF1Bo
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 0f5947b3f28ba40cd479df463c843f7e99155d5e
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 0%

---

# Colocación de capas{#layer-placement}

Las capas se colocan alineando el origen de la capa (origin=) con el origen de la capa de fondo en un desplazamiento especificado por pos=.

Si el origen de la capa no se especifica explícitamente para una capa de imagen, se calcula de la siguiente manera:

1. Determine el anclaje de la imagen. Use `anchor=` o, si no se especifica, `catalog::Anchor`.
1. Si se define el anclaje de imagen, aplique las transformaciones de capa y `extend=` para convertirlo en un origin= value.
1. Si no se define ningún anclaje de imagen, el origen de la capa se coloca en el centro del rectángulo de capa (después de aplicar `extend=`).

![Imagen de colocación de capas](assets/layerplacement.png)
