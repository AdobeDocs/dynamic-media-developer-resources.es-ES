---
description: Establecer margen de sangrado. Establece el margen de sangrado que se establece en el archivo PDF.
solution: Experience Manager
title: margen de sangrado
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# margen de sangrado{#bleedmargin}

Establecer margen de sangrado. Establece el margen de sangrado que se establece en el archivo PDF.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en puntos

De manera predeterminada, `bleedMargin` está establecido en el tamaño completo del documento definido por `viewWidth` y `viewHeight`. Los valores *[!DNL left]*, *[!DNL bottom]* y *[!DNL right]* tienen de manera predeterminada el valor *[!DNL top]* si no se especifican.
