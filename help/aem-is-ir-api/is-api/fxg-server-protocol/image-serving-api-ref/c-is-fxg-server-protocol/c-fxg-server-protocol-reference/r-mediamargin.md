---
description: Establezca el margen de medios. Establece el margen de medios definido en el archivo PDF.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

Establezca el margen de medios. Establece el margen de medios definido en el archivo PDF.

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en puntos

De forma predeterminada, el `mediaMargin` se establece en el tamaño completo del documento definido por `viewWidth` y `viewHeight`. Los valores *[!DNL left]*, *[!DNL bottom]* y *[!DNL right]* se asignan de forma predeterminada al valor *[!DNL top]* si no se especifica.
