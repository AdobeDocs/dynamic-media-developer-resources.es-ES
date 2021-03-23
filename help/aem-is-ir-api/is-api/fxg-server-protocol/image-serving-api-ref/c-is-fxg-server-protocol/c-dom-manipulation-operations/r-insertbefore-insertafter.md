---
description: Establezca XML antes o después de un nodo.
seo-description: Establezca XML antes o después de un nodo.
seo-title: insertBefore,insertAfter
solution: Experience Manager
title: insertBefore,insertAfter
uuid: 5ac0f675-333b-4f85-abe0-642cf96de425
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 2%

---


# insertBefore,insertAfter{#insertbefore-insertafter}

Establezca XML antes o después de un nodo.

`insertBefore=<xml>, insertAfter=<xml>`

Si un elemento de nodo FXG tiene un `s7:elementID` definido, podemos agregar fragmentos XML antes o después de ese nodo con este comando.

## Ejemplo {#section-1fc8d4135ef94b60b838391e1568e70e}

Si tenemos una etiqueta de grupo como esta:

`<Group visible="true" s7:elementID="inner_shape">`

entonces:

`insertBefore.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

da como resultado:

`<Rect height="75" rotation="0" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" width="75" x="74.354" y="182.762"><fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill></Rect><Group s7:elementID="inner_shape" visible="true">`

`insertAfter.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

da como resultado:

`<Group s7:elementID="inner_shape" visible="true"> <Rect ai:knockout="0" d:userLabel="Background" height="392.581" visible="true" width="319.953" x="0.75" y="0.75"> <fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill> </Rect>`
