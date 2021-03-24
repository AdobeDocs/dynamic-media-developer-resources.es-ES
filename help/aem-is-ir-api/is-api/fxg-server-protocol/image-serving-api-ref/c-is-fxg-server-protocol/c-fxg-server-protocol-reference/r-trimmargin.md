---
description: Establezca el margen de recorte. Define el margen de recorte que se establece en el archivo PDF.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# trimMargin{#trimmargin}

Establezca el margen de recorte. Define el margen de recorte que se establece en el archivo PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en puntos

De forma predeterminada, el `trimMargin` se establece en el tamaño completo del documento definido por `viewWidth` y `viewHeight`. Los valores *[!DNL left]*, *[!DNL bottom]* y *[!DNL right]* se asignan de forma predeterminada al valor *[!DNL top]* si no se especifica.
