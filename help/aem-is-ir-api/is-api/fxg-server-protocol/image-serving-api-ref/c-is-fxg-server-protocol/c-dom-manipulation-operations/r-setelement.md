---
description: Configure XML en un elementID de s7.
seo-description: Configure XML en un elementID de s7.
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setElement{#setelement}

Establezca XML en s7:elementID.

`setElement.elementID=<XML>`

Si un elemento de nodo FXG tiene una `s7:elementID` definición, el `<XML>` valor se reemplaza como elemento secundario. The `<XML>` must be encoded.

## Ejemplo {#section-f23a998b18994dd3b5d4e1965718db9f}

Supongamos que se define un `s7:elementID="group2"` atributo para un `Group` nodo y que lo siguiente es válido:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

En este ejemplo se eliminan todos los elementos secundarios del `group2`nodo y se reemplaza por un nuevo nodo secundario `TextGraphic` .
