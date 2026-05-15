---
title: setElement
description: Establezca XML en un elementID de s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
TQID: 'https://experienceleague.adobe.com/bLej-B1yRcTdFFXhaigx4Zf9ubwx9LkR31a9Rqdr0Zs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 62
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
