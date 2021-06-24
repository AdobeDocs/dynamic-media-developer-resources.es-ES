---
description: Si req=img, el tamaño del lienzo de composición viene determinado completamente por el tamaño de la capa 0.
solution: Experience Manager
title: El lienzo de composición
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# El lienzo de composición{#the-compositing-canvas}

Si req=img, el tamaño del lienzo de composición viene determinado completamente por el tamaño de la capa 0.

Si el `size=` para la capa 0 no se especifica explícitamente, las transformaciones de capa se utilizan para calcular el tamaño del lienzo de composición (ver abajo).

Si `req=tmb`, el tamaño del lienzo de composición viene determinado por el `size=` especificado para la capa 0 o, si no se especifica el tamaño, el tamaño del lienzo de composición se establece en el directorio de vista (consulte a continuación).
