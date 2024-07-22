---
description: Elimine cualquier atributo de un elementID s7 determinado.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 2%

---

# deleteAttr{#deleteattr}

Elimine cualquier atributo de un s7:elementID determinado.

`deleteAttr.elementID={attributeName%26attributeName}`

Si un elemento de nodo FXG tiene un `s7:elementID` definido, los atributos de ese nodo se pueden eliminar con este comando.

## Ejemplo {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

Este ejemplo quita los atributos *[!DNL x]*, *[!DNL y]* y *[!DNL visible]* del nodo FXG original.
