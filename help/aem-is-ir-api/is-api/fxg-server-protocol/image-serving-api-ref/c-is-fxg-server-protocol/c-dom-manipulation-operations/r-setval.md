---
description: Establezca el valor del nodo de texto para s7 elementID.
seo-description: Establezca el valor del nodo de texto para s7 elementID.
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# setVal{#setval}

Establezca el valor del nodo de texto para s7:elementID.

`setVal.elementID= *[!DNL value]*`

Si un elemento de nodo FXG tiene definida una `s7:elementID`, se puede manipular el valor de texto para ese nodo.

## Ejemplo {#section-f574fd66dedd4a219aa537d7bdabea23}

Supongamos que se define un atributo `s7:elementID="paragraph1"` para un nodo `TextGraphic` y que lo siguiente es válido:

`&setVal.paragraph=Hello`

En este ejemplo se establece el valor de texto del nodo de párrafo en &quot;Hello&quot;.
