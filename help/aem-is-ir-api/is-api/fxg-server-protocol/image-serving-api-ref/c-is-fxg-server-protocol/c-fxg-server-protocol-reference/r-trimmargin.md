---
description: Establezca el margen de corte. Define el margen de recorte que se establece en el archivo PDF.
seo-description: Establezca el margen de corte. Define el margen de recorte que se establece en el archivo PDF.
seo-title: trimMargin
solution: Experience Manager
title: trimMargin
topic: Scene7 Image Serving - Image Rendering API
uuid: af94f9e8-a32e-439a-817a-a40aa8dc7dd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# trimMargin{#trimmargin}

Establezca el margen de corte. Define el margen de recorte que se establece en el archivo PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en puntos

De forma predeterminada, `trimMargin` se establece en el tamaño completo del documento definido por `viewWidth` y `viewHeight`. Los valores *[!DNL left]*, *[!DNL bottom]* y *[!DNL right]* tienen el valor predeterminado *[!DNL top]* si no se especifican.
