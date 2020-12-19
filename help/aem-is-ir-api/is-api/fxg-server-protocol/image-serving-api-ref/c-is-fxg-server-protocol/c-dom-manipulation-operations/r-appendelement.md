---
description: Anexe XML a un elementID de s7.
seo-description: Anexe XML a un elementID de s7.
seo-title: appendElement
solution: Experience Manager
title: appendElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 062c8288-4517-42a1-9f9f-f3c7bbb4b63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---


# appendElement{#appendelement}

Anexe XML a un ID de elemento de s7.

`appendElement.elementID=<XML>`

Si un elemento de nodo FXG tiene definida una `s7:elementID`, el valor `<XML>` se anexa como un elemento secundario. El `<XML>` debe estar codificado.

## Ejemplo {#section-4368570aa198485d91b73b4d0741478f}

Supongamos que se define un atributo `s7:elementID="group1"` para un nodo de grupo y que lo siguiente es válido:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Este ejemplo anexa un elemento secundario de gráfico de texto a `group1`.
