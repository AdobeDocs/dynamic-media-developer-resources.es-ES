---
description: Si req=img, el tamaño del lienzo de composición se determina completamente por el tamaño de la capa 0.
seo-description: Si req=img, el tamaño del lienzo de composición se determina completamente por el tamaño de la capa 0.
seo-title: El lienzo de composición
solution: Experience Manager
title: El lienzo de composición
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# El lienzo de composición{#the-compositing-canvas}

Si req=img, el tamaño del lienzo de composición se determina completamente por el tamaño de la capa 0.

Si no se especifica explícitamente el `size=` para la capa 0, las transformaciones de capa se utilizan para calcular el tamaño del lienzo de composición (véase más abajo).

Si `req=tmb`el tamaño del lienzo de composición está determinado por el tamaño `size=` especificado para la capa 0 o, si no se especifica el tamaño, el tamaño del lienzo de composición se establece en el rectángulo de vista (véase a continuación).
