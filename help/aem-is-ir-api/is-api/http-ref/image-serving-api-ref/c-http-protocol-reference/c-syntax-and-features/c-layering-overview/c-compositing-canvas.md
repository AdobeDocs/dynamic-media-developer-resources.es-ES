---
description: Las capas se componen en el orden especificado por el comando layer=, donde las capas con mayor número ocultan las con menor número.
seo-description: Las capas se componen en el orden especificado por el comando layer=, donde las capas con mayor número ocultan las con menor número.
seo-title: El lienzo de composición
solution: Experience Manager
title: El lienzo de composición
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# El lienzo de composición{#the-compositing-canvas}

Las capas se componen en el orden especificado por el comando layer=, donde las capas con mayor número ocultan las con menor número.

La capa 0 constituye la capa de fondo, que siempre es necesaria y que define el tamaño de la imagen compuesta. Se permite cualquiera de los tipos de capas para la capa 0. El tamaño de la capa 0 debe definirse, ya sea explícitamente `size=` o implícitamente, en función de la imagen o el texto del contenido. Las áreas de otras capas que queden fuera del área de la capa 0 no se incluirán en la imagen de salida.

>[!NOTE]
>
>Después de acoplar todas las capas, la imagen compuesta se convierte en la imagen de respuesta final, tal como se especifica con los comandos y atributos [de](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)vista.

