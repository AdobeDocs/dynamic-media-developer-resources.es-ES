---
description: La mayoría de los materiales se pueden colorear dinámicamente.
solution: Experience Manager
title: Colorización de materiales
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Colorización de materiales{#colorizing-materials}

La mayoría de los materiales se pueden colorear dinámicamente.

El algoritmo de colorización es bastante simplista y funciona mejor para imágenes de material con un rango de matiz limitado. Para colorear un material, el renderizador simplemente resta el valor `bgc=` y agrega el valor `color=` a cada valor de píxel.

La colorización está deshabilitada si no se especifica `color=`. `bgc=` es ignorado por los materiales del gabinete; se utiliza el valor de color base incrustado en el  [!DNL vnc] archivo.
