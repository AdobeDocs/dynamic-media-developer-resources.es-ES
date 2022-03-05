---
title: Colorización de materiales
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

# Colorización de materiales{#colorizing-materials}

La mayoría de los materiales se pueden colorear dinámicamente.

El algoritmo de colorización es simplista y funciona mejor para imágenes de material con un rango de matiz limitado. Para colorear un material, el renderizador simplemente resta la variable `bgc=` y agrega la variable `color=` a cada valor de píxel.

La organización está desactivada si `color=` no se ha especificado. La variable `bgc=` los materiales del gabinete ignoran el atributo; el valor de color base incrustado en la variable [!DNL vnc] se utiliza en su lugar.
