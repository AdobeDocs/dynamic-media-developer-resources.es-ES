---
title: setAttr
description: Establezca cualquier atributo para un elementID de s7 determinado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '99'
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
