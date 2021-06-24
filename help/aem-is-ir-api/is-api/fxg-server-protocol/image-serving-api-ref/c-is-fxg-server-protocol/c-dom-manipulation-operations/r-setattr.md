---
description: Establezca cualquier atributo para un elementID de s7 determinado.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# setAttr{#setattr}

Establezca cualquier atributo para un s7:elementID determinado.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Si un elemento de nodo FXG tiene un `s7:elementID` definido, puede manipular los atributos para ese nodo. Puede establecer todos los pares de atributos/valores que desee. Los atributos no necesitan estar definidos en el FXG, pero deben ser válidos para el elemento node . Todos los valores entre `{}` deben estar Escaped.

## Ejemplo {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supongamos que se define un atributo `s7:elementID="Group1"` para un nodo `BitmapGraphic` y que lo siguiente es válido:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

En este ejemplo se establecen los valores *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* y *[!DNL scaleY]* para `BitmapGraphic` y se anula cualquier valor existente.
