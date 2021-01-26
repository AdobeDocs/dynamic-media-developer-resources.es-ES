---
description: Si req=img, el tamaño del lienzo de composición se determina completamente por el tamaño de la capa 0.
seo-description: Si req=img, el tamaño del lienzo de composición se determina completamente por el tamaño de la capa 0.
seo-title: El lienzo de composición
solution: Experience Manager
title: El lienzo de composición
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# El lienzo de composición{#the-compositing-canvas}

Si req=img, el tamaño del lienzo de composición se determina completamente por el tamaño de la capa 0.

Si el `size=` para la capa 0 no se especifica explícitamente, las transformaciones de capa se utilizan para calcular el tamaño del lienzo de composición (ver más abajo).

Si `req=tmb`, el tamaño del lienzo de composición viene determinado por el `size=` especificado para la capa 0 o, si no se especifica el tamaño, el tamaño del lienzo de composición se establece en el rectángulo de vista (véase más adelante).
