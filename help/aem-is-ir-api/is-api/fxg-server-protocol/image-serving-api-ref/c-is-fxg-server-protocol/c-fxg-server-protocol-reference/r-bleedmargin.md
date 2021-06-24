---
description: Establezca el margen de sangrado. Establece el margen de sangrado definido en el archivo PDF.
solution: Experience Manager
title: bleedmargin
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# bleedmargin{#bleedmargin}

Establezca el margen de sangrado. Establece el margen de sangrado definido en el archivo PDF.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en puntos

De forma predeterminada, el `bleedMargin` se establece en el tamaño completo del documento definido por `viewWidth` y `viewHeight`. Los valores *[!DNL left]*, *[!DNL bottom]* y *[!DNL right]* se asignan de forma predeterminada al valor *[!DNL top]* si no se especifica.
