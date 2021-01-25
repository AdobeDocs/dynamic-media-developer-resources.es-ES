---
description: Elimine cualquier atributo de un elementID de s7 determinado.
seo-description: Elimine cualquier atributo de un elementID de s7 determinado.
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 1%

---


# deleteAttr{#deleteattr}

Elimine cualquier atributo de un s7:elementID determinado.

`deleteAttr.elementID={attributeName%26attributeName}`

Si un elemento de nodo FXG tiene definida una `s7:elementID`, los atributos de ese nodo se pueden eliminar con este comando.

## Ejemplo {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

Este ejemplo elimina los atributos *[!DNL x]*, *[!DNL y]* y *[!DNL visible]* del nodo FXG original.
