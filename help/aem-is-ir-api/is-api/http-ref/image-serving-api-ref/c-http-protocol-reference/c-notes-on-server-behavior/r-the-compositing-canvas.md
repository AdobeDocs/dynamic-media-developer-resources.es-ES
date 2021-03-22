---
description: Si req=img, el tamaño del lienzo de composición viene determinado completamente por el tamaño de la capa 0.
seo-description: Si req=img, el tamaño del lienzo de composición viene determinado completamente por el tamaño de la capa 0.
seo-title: El lienzo de composición
solution: Experience Manager
title: El lienzo de composición
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# El lienzo de composición{#the-compositing-canvas}

Si req=img, el tamaño del lienzo de composición viene determinado completamente por el tamaño de la capa 0.

Si el `size=` para la capa 0 no se especifica explícitamente, las transformaciones de capa se utilizan para calcular el tamaño del lienzo de composición (ver abajo).

Si `req=tmb`, el tamaño del lienzo de composición viene determinado por el `size=` especificado para la capa 0 o, si no se especifica el tamaño, el tamaño del lienzo de composición se establece en el directorio de vista (consulte a continuación).
