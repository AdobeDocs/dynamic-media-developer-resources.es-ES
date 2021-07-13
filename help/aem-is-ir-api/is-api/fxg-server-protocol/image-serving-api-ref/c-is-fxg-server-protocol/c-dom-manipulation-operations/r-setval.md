---
description: Establezca el valor del nodo de texto para s7 elementID.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
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
