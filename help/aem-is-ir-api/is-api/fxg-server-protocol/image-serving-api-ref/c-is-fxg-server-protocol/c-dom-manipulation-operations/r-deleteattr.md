---
description: Elimine cualquier atributo de un elementID de s7 determinado.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---

# deleteAttr{#deleteattr}

Elimine cualquier atributo de un s7:elementID determinado.

`deleteAttr.elementID={attributeName%26attributeName}`

Si un elemento de nodo FXG tiene un `s7:elementID` definido, los atributos de ese nodo se pueden eliminar con este comando.

## Ejemplo {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

Este ejemplo elimina los atributos *[!DNL x]*, *[!DNL y]* y *[!DNL visible]* del nodo FXG original.
