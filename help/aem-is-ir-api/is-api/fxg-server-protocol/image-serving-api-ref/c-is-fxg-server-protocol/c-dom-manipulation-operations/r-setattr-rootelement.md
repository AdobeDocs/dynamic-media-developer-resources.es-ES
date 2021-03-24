---
description: Establezca atributos en el elemento raíz FXG.
solution: Experience Manager
title: setAttr.rootElement
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---


# setAttr.rootElement{#setattr-rootelement}

Establezca atributos en el elemento raíz FXG.

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

Este comando puede manipular atributos del elemento raíz.

## Ejemplo {#section-2758a6e316c34b99b13b02147e5973bb}

Si tenemos el siguiente elemento raíz:

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

Después de aplicar el siguiente comando:

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

El elemento raíz ahora se cambia a lo siguiente:

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`
