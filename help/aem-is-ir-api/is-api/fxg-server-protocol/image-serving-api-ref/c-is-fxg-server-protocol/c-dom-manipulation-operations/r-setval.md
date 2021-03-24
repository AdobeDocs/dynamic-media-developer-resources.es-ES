---
description: Establezca el valor del nodo de texto para s7 elementID.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
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
