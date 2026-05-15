---
description: Las capas se componen en el orden especificado por el comando layer=, donde las capas con números más altos ocultan las capas con números más bajos.
solution: Experience Manager
title: El lienzo de composición
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
TQID: 'https://experienceleague.adobe.com/WNvq6dLRetz3iEbtP0ugmOPagUfTCaa5eXdB3lEzEaQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 0%

---

# El lienzo de composición{#the-compositing-canvas}

Las capas se componen en el orden especificado por el comando layer=, donde las capas con números más altos ocultan las capas con números más bajos.

La capa 0 constituye la capa de fondo, que siempre es necesaria y que define el tamaño de la imagen compuesta. Se permite cualquiera de los tipos de capa para la capa 0. Se debe definir el tamaño de la capa 0, ya sea de forma explícita con `size=` o implícitamente, en función de la imagen o el texto del contenido. Las áreas de otras capas que se encuentran fuera del área de la capa 0 no se incluyen en la imagen de salida.

>[!NOTE]
>
>Una vez acopladas todas las capas, la imagen compuesta se convierte en la imagen de respuesta final, tal como se especifica con los [comandos y atributos de vista](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
