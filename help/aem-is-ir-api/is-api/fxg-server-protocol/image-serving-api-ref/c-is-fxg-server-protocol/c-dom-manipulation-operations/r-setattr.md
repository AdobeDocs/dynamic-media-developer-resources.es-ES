---
description: Establezca cualquier atributo para un elementID de s7 determinado.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# setAttr{#setattr}

Establezca cualquier atributo para un s7:elementID determinado.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Si un elemento de nodo FXG tiene un `s7:elementID` definida, puede manipular los atributos de ese nodo. Puede establecer tantos pares de atributo/valor como desee. No es necesario definir los atributos en el FXG, pero deben ser válidos para el elemento node. Todos los valores intermedios `{}` debe ser Escaped.

## Ejemplo {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supongamos que `s7:elementID="Group1"` El atributo está definido para `BitmapGraphic` , lo siguiente es válido:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Este ejemplo establece el *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]*, y *[!DNL scaleY]* para el `BitmapGraphic` y anula los valores existentes.
