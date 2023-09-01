---
title: setVal
description: Establezca el valor del nodo de texto para el elementID de s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 1%

---

# setVal{#setval}

Establezca el valor del nodo de texto para s7:elementID.

`setVal.elementID= *[!DNL value]*`

Si un elemento de nodo FXG tiene un `s7:elementID` definido, el valor de texto para ese nodo se puede manipular.

## Ejemplo {#section-f574fd66dedd4a219aa537d7bdabea23}

Supongamos que `s7:elementID="paragraph1"` El atributo está definido para `TextGraphic` y, a continuación, lo siguiente es válido:

`&setVal.paragraph=Hello`

En este ejemplo se establece el valor de texto del nodo de párrafo en &quot;Hello&quot;.
