---
description: La mayoría de los materiales se pueden colorear dinámicamente.
seo-description: La mayoría de los materiales se pueden colorear dinámicamente.
seo-title: Colorización de materiales
solution: Experience Manager
title: Colorización de materiales
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---


# Colorear materiales{#colorizing-materials}

La mayoría de los materiales se pueden colorear dinámicamente.

El algoritmo de colorización es bastante simplista y funciona mejor para imágenes de material con un rango de matiz limitado. Para colorear un material, el renderizador simplemente resta el valor `bgc=` y agrega el valor `color=` a cada valor de píxel.

La colorización está deshabilitada si no se especifica `color=`. `bgc=` es ignorado por los materiales del gabinete; se utiliza el valor de color base incrustado en el  [!DNL vnc] archivo.
