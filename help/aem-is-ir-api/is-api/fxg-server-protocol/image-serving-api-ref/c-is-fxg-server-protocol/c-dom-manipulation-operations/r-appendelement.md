---
title: appendElement
description: Anexe XML a un elementID de s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---

# appendElement{#appendelement}

Anexe XML a s7:elementID.

`appendElement.elementID=<XML>`

Si un elemento de nodo FXG tiene un `s7:elementID` definida, la variable `<XML>` El valor de se anexa como elemento secundario. El `<XML>` debe estar codificado.

## Ejemplo {#section-4368570aa198485d91b73b4d0741478f}

Supongamos que `s7:elementID="group1"` El atributo está definido para un nodo Group y, a continuación, es válido lo siguiente:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

En este ejemplo se anexa un elemento secundario de gráfico de texto a `group1`.
