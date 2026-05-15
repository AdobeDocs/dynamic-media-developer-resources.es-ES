---
title: setAttr
description: Establezca cualquier atributo para un elementID de s7 determinado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
TQID: 'https://experienceleague.adobe.com/0O1uOLXsh-5PkBnXugpQYJHDAZep49WO3AA4hjClODk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 1%

---

# setAttr{#setattr}

Establezca cualquier atributo para un s7:elementID determinado.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Si un elemento de nodo FXG tiene un `s7:elementID` definido, puede manipular los atributos de ese nodo. Puede establecer tantos pares de atributo/valor como desee. No es necesario definir los atributos en el FXG, pero deben ser válidos para el elemento node. Se deben escapar todos los valores comprendidos entre `{}`.

## Ejemplo {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supongamos que se ha definido un atributo `s7:elementID="Group1"` para un nodo `BitmapGraphic` y que lo siguiente es válido:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Este ejemplo establece *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* y *[!DNL scaleY]* para `BitmapGraphic` y anula los valores existentes.
