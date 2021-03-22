---
description: Las capas se componen en el orden especificado por el comando layer=, donde las capas con mayor número ocultan las que tienen menor número.
seo-description: Las capas se componen en el orden especificado por el comando layer=, donde las capas con mayor número ocultan las que tienen menor número.
seo-title: El lienzo de composición
solution: Experience Manager
title: El lienzo de composición
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# El lienzo de composición{#the-compositing-canvas}

Las capas se componen en el orden especificado por el comando layer=, donde las capas con mayor número ocultan las que tienen menor número.

La capa 0 constituye la capa de fondo, que siempre es necesaria y que define el tamaño de la imagen compuesta. Se permite cualquiera de los tipos de capa para la capa 0. El tamaño de la capa 0 debe definirse, ya sea explícitamente utilizando `size=` o implícitamente, en función de la imagen de contenido o el texto. No se incluirán en la imagen de salida todas las áreas de otras capas que queden fuera del área de la capa 0.

>[!NOTE]
>
>Una vez aplanadas todas las capas, la imagen compuesta se convierte a la imagen de respuesta final, tal como se especifica con los comandos y atributos [view](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).

