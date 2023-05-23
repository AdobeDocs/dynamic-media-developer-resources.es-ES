---
description: Las capas se componen en el orden especificado por el comando layer=, donde las capas con números más altos ocultan las capas con números más bajos.
solution: Experience Manager
title: El lienzo de composición
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# El lienzo de composición{#the-compositing-canvas}

Las capas se componen en el orden especificado por el comando layer=, donde las capas con números más altos ocultan las capas con números más bajos.

La capa 0 constituye la capa de fondo, que siempre es necesaria y que define el tamaño de la imagen compuesta. Se permite cualquiera de los tipos de capa para la capa 0. Se debe definir el tamaño de la capa 0, ya sea explícitamente utilizando `size=` o implícitamente, en función de la imagen o el texto del contenido. Las áreas de otras capas que queden fuera del área de la capa 0 no se incluirán en la imagen de salida.

>[!NOTE]
>
>Una vez aplanadas todas las capas, la imagen compuesta se convierte en la imagen de respuesta final, tal como se especifica con la variable [ver comandos y atributos](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
