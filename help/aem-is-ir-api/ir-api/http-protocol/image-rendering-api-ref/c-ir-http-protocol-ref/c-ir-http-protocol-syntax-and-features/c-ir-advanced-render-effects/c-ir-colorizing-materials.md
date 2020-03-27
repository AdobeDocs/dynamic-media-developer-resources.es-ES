---
description: La mayoría de los materiales se pueden colorear dinámicamente.
seo-description: La mayoría de los materiales se pueden colorear dinámicamente.
seo-title: Colorear materiales
solution: Experience Manager
title: Colorear materiales
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Colorear materiales{#colorizing-materials}

La mayoría de los materiales se pueden colorear dinámicamente.

El algoritmo de colorización es bastante simplista y funciona mejor para imágenes de material con un rango de tono limitado. Para colorear un material, el procesador simplemente resta el `bgc=` valor y agrega el valor `color=` a cada valor de píxel.

La colorización se desactiva si no `color=` se especifica. `bgc=` se ignora por los materiales del gabinete; en su lugar, se utiliza el valor de color base incrustado en el [!DNL vnc] archivo.
