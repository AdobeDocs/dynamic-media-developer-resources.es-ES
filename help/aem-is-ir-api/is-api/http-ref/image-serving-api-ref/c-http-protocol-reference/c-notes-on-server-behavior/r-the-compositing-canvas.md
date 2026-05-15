---
description: Si req=img, el tamaño del lienzo de composición viene determinado totalmente por el tamaño de la capa 0.
solution: Experience Manager
title: El lienzo de composición
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
TQID: 'https://experienceleague.adobe.com/62uvC05pApoYR5lY4A-KA5RHmW8Xz0r2-2yvOpdAkOo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# El lienzo de composición{#the-compositing-canvas}

Si req=img, el tamaño del lienzo de composición viene determinado totalmente por el tamaño de la capa 0.

Si no se especifica explícitamente el `size=` para la capa 0, las transformaciones de capa se utilizan para calcular el tamaño del lienzo de composición (ver a continuación).

Si `req=tmb`, el tamaño del lienzo de composición viene determinado por el `size=` especificado para la capa 0 o, si no se especifica el tamaño, el tamaño del lienzo de composición se establece en la vista recta (ver a continuación).
