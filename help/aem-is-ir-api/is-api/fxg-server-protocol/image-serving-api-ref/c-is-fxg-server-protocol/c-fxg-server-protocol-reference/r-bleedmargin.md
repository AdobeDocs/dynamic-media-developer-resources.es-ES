---
description: Establecer margen de sangrado. Establece el margen de sangrado que se establece en el archivo PDF.
solution: Experience Manager
title: margen de sangrado
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
TQID: 'https://experienceleague.adobe.com/Lghb-4jpksjewoUjBD-SE9UqsD6AX6WFwb2sbkCobXE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 0%

---

# margen de sangrado{#bleedmargin}

Establecer margen de sangrado. Establece el margen de sangrado que se establece en el archivo PDF.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` en puntos

De manera predeterminada, `bleedMargin` está establecido en el tamaño completo del documento definido por `viewWidth` y `viewHeight`. Los valores *[!DNL left]*, *[!DNL bottom]* y *[!DNL right]* tienen de manera predeterminada el valor *[!DNL top]* si no se especifican.
