---
description: La mayoría de los materiales se pueden colorear dinámicamente.
solution: Experience Manager
title: Colorización de materiales
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Colorear materiales{#colorizing-materials}

La mayoría de los materiales se pueden colorear dinámicamente.

El algoritmo de colorización es bastante simplista y funciona mejor para imágenes de material con un rango de matiz limitado. Para colorear un material, el renderizador simplemente resta el valor `bgc=` y agrega el valor `color=` a cada valor de píxel.

La colorización está deshabilitada si no se especifica `color=`. `bgc=` es ignorado por los materiales del gabinete; se utiliza el valor de color base incrustado en el  [!DNL vnc] archivo.
