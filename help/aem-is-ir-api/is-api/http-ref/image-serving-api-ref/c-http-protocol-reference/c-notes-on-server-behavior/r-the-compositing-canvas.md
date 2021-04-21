---
description: Si req=img, el tamaño del lienzo de composición viene determinado completamente por el tamaño de la capa 0.
solution: Experience Manager
title: El lienzo de composición
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# El lienzo de composición{#the-compositing-canvas}

Si req=img, el tamaño del lienzo de composición viene determinado completamente por el tamaño de la capa 0.

Si el `size=` para la capa 0 no se especifica explícitamente, las transformaciones de capa se utilizan para calcular el tamaño del lienzo de composición (ver abajo).

Si `req=tmb`, el tamaño del lienzo de composición viene determinado por el `size=` especificado para la capa 0 o, si no se especifica el tamaño, el tamaño del lienzo de composición se establece en el directorio de vista (consulte a continuación).
