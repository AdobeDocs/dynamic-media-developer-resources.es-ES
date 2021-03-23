---
description: Establezca XML en un elementID de s7.
seo-description: Establezca XML en un elementID de s7.
seo-title: setElement
solution: Experience Manager
title: setElement
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---


# setElement{#setelement}

Establezca XML en s7:elementID.

`setElement.elementID=<XML>`

Si un elemento de nodo FXG tiene un `s7:elementID` definido, el valor `<XML>` se reemplaza como elemento secundario. El `<XML>` debe estar codificado.

## Ejemplo {#section-f23a998b18994dd3b5d4e1965718db9f}

Supongamos que se define un atributo `s7:elementID="group2"` para un nodo `Group` y que lo siguiente es válido:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

En este ejemplo se eliminan todos los elementos secundarios del nodo `group2`y se reemplaza con el nuevo nodo secundario `TextGraphic`.
