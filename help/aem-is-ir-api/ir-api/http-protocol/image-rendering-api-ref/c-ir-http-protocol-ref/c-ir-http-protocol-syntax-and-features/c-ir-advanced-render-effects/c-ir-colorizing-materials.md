---
title: Materiales colorantes
description: La mayoría de los materiales se pueden colorear dinámicamente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# Materiales colorantes{#colorizing-materials}

La mayoría de los materiales se pueden colorear dinámicamente.

El algoritmo de colorización es simplista y funciona mejor con imágenes de material que tienen un rango de tonalidades limitado. Para colorear un material, el procesador simplemente resta el valor `bgc=` y agrega el valor `color=` a cada valor de píxel.

La colorización está deshabilitada si no se especifica `color=`. Los materiales del archivador omiten el atributo `bgc=`; en su lugar se utiliza el valor de color base incrustado en el archivo [!DNL vnc].
