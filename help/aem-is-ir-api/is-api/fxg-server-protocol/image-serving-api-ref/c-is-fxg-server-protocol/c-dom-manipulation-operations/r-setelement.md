---
title: setElement
description: Establezca XML en un elementID de s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# setElement{#setelement}

Establezca XML en s7:elementID.

`setElement.elementID=<XML>`

Si un elemento de nodo FXG tiene un `s7:elementID` definida, la variable `<XML>` El valor de se sustituye como elemento secundario. El `<XML>` debe estar codificado.

## Ejemplo {#section-f23a998b18994dd3b5d4e1965718db9f}

Supongamos que `s7:elementID="group2"` El atributo está definido para `Group` y, a continuación, lo siguiente es válido:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

En este ejemplo se eliminan todos los elementos secundarios del `group2`y lo reemplaza por el nuevo `TextGraphic` nodo secundario.
