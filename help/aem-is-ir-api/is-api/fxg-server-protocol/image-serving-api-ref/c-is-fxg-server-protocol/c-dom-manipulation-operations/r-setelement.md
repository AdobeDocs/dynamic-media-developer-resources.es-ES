---
title: setElement
description: Establezca XML en un elementID de s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# setElement{#setelement}

Establezca XML en s7:elementID.

`setElement.elementID=<XML>`

Si un elemento de nodo FXG tiene un `s7:elementID` definido, el valor `<XML>` se reemplaza como elemento secundario. Se debe codificar `<XML>`.

## Ejemplo {#section-f23a998b18994dd3b5d4e1965718db9f}

Supongamos que se ha definido un atributo `s7:elementID="group2"` para un nodo `Group` y que es válido lo siguiente:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Este ejemplo quita todos los elementos secundarios del nodo `group2` y lo reemplaza por el nuevo nodo secundario `TextGraphic`.
