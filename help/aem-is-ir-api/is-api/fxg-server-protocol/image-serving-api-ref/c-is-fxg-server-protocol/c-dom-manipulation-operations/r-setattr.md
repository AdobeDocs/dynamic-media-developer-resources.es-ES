---
description: Configure cualquier atributo para un elementID de s7 determinado.
seo-description: Configure cualquier atributo para un elementID de s7 determinado.
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# setAttr{#setattr}

Configure cualquier atributo para un s7:elementID determinado.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Si un elemento de nodo FXG tiene definida una `s7:elementID`, puede manipular los atributos para ese nodo. Puede establecer tantos pares de atributos y valores como desee. No es necesario definir los atributos en FXG, pero deben ser válidos para el elemento node. Todos los valores entre `{}` deben ser Escapados.

## Ejemplo {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supongamos que se define un atributo `s7:elementID="Group1"` para un nodo `BitmapGraphic` y que lo siguiente es válido:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Este ejemplo establece los valores *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* y *[!DNL scaleY]* para `BitmapGraphic` y anula los valores existentes.
