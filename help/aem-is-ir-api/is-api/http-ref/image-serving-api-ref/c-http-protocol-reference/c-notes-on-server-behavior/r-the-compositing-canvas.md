---
description: Si req=img, el tamaño del lienzo de composición viene determinado totalmente por el tamaño de la capa 0.
solution: Experience Manager
title: El lienzo de composición
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# El lienzo de composición{#the-compositing-canvas}

Si req=img, el tamaño del lienzo de composición viene determinado totalmente por el tamaño de la capa 0.

Si no se especifica explícitamente el `size=` para la capa 0, las transformaciones de capa se utilizan para calcular el tamaño del lienzo de composición (ver a continuación).

Si `req=tmb`, el tamaño del lienzo de composición viene determinado por el `size=` especificado para la capa 0 o, si no se especifica el tamaño, el tamaño del lienzo de composición se establece en la vista recta (ver a continuación).
