---
description: Después de instalar el servicio de imágenes de Scene7, debe comprobar la instalación.
seo-description: Después de instalar el servicio de imágenes de Scene7, debe comprobar la instalación.
seo-title: Verificación de la instalación
solution: Experience Manager
title: Verificación de la instalación
topic: Scene7 Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# Verificación de la instalación{#verifying-the-installation}

Después de instalar el servicio de imágenes de Scene7, debe comprobar la instalación.

El servidor de imágenes se instala como un servicio de Windows.

1. Abra el Panel de control de Campaign Servicios y compruebe que &quot;Scene7 Image Serving&quot; esté presente con el estado &quot;Started&quot; (Iniciado).
1. Abra un explorador de Internet en el mismo host o en otro diferente y compruebe las respuestas predeterminadas del servidor:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/procesar]

Compruebe la presencia de elementos &quot; `imageServer.`&quot; en la respuesta, lo que indica que el servidor de imágenes está escuchando.
>Se puede realizar una verificación adicional utilizando las páginas de muestra de los paquetes Documentación y Demostración, si están instalados.

