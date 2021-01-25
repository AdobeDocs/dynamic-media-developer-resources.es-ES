---
description: La mayoría de los materiales se pueden colorear dinámicamente.
seo-description: La mayoría de los materiales se pueden colorear dinámicamente.
seo-title: Colorear materiales
solution: Experience Manager
title: Colorear materiales
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Colorear materiales{#colorizing-materials}

La mayoría de los materiales se pueden colorear dinámicamente.

El algoritmo de colorización es bastante simplista y funciona mejor para imágenes de material con un rango de tono limitado. Para colorear un material, el procesador simplemente resta el valor `bgc=` y agrega el valor `color=` a cada valor de píxel.

La colorización está deshabilitada si no se especifica `color=`. `bgc=` se ignora por los materiales del gabinete; en su lugar, se utiliza el valor de color base incrustado en el  [!DNL vnc] archivo.
