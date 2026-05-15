---
description: Elimine cualquier atributo de un elementID s7 determinado.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
TQID: 'https://experienceleague.adobe.com/dQN741iV4LtlEeq3R4tAnPcBHK-AHrzD-jv7AQ4a5ls'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 48
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
