---
title: Materiales colorantes
description: La mayoría de los materiales se pueden colorear dinámicamente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
TQID: 'https://experienceleague.adobe.com/MGmuOj214tFPKeSGwz33pGn2m0B0fme1Cq-umlxG9v0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# Materiales colorantes{#colorizing-materials}

La mayoría de los materiales se pueden colorear dinámicamente.

El algoritmo de colorización es simplista y funciona mejor con imágenes de material que tienen un rango de tonalidades limitado. Para colorear un material, el procesador simplemente resta el valor `bgc=` y agrega el valor `color=` a cada valor de píxel.

La colorización está deshabilitada si no se especifica `color=`. Los materiales del archivador omiten el atributo `bgc=`; en su lugar se utiliza el valor de color base incrustado en el archivo [!DNL vnc].
