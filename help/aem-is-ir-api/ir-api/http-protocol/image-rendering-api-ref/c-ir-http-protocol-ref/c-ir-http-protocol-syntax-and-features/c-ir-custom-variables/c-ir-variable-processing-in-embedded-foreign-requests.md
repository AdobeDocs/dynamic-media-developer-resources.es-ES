---
title: Procesamiento de variables en solicitudes externas incrustadas
description: Las referencias $var$ que se producen en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituyen por valores de definición de variable coincidentes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
TQID: 'https://experienceleague.adobe.com/-0KT9d6qz9-8d41vKNgbCYUKQQLBRaLE-0TFmyIvRCM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# Procesamiento de variables en solicitudes externas incrustadas{#variable-processing-in-embedded-foreign-requests}

Cualquier referencia `$var$` que aparezca en cualquier lugar dentro de las llaves de una solicitud externa incrustada se sustituirá con valores de definición de variable coincidentes.

Permite colocar solicitudes externas incrustadas en una plantilla de un catálogo de imágenes.

Los valores de variable que se sustituyen en solicitudes externas suelen tener una codificación doble, ya que no se aplica ninguna codificación adicional antes de que el servidor intente transmitir la dirección URL externa final.
