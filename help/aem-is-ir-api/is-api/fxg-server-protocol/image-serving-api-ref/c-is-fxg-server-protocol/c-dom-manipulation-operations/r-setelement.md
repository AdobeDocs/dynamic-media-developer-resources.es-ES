---
description: Establezca XML en un elementID de s7.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
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
