---
description: Establezca el valor del nodo de texto para s7 elementID.
seo-description: Establezca el valor del nodo de texto para s7 elementID.
seo-title: setVal
solution: Experience Manager
title: setVal
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---


# setVal{#setval}

Establezca el valor del nodo de texto para s7:elementID.

`setVal.elementID= *[!DNL value]*`

Si un elemento de nodo FXG tiene un `s7:elementID` definido, el valor de texto para ese nodo puede manipularse.

## Ejemplo {#section-f574fd66dedd4a219aa537d7bdabea23}

Supongamos que se define un atributo `s7:elementID="paragraph1"` para un nodo `TextGraphic` y que lo siguiente es válido:

`&setVal.paragraph=Hello`

En este ejemplo se establece el valor de texto del nodo de párrafo en &quot;Hello&quot;.
