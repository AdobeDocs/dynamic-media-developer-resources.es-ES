---
description: Existen dos opciones para iniciar o detener el servicio de imágenes en Linux.
seo-description: Existen dos opciones para iniciar o detener el servicio de imágenes en Linux.
seo-title: Inicio o parada en Linux
solution: Experience Manager
title: Inicio o parada en Linux
topic: Scene7 Image Serving - Image Rendering API
uuid: 92cf60c4-3f80-42bc-b135-17bc22ba151e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# Inicio o parada en Linux{#starting-or-stopping-on-linux}

Existen dos opciones para iniciar o detener el servicio de imágenes en Linux.

* La secuencia de comandos para inicio, parada y verificación del estado del servicio de imágenes se encuentra en la carpeta [!DNL ImageServing/bin]:

   `ImageServing.sh {start|stop|restart|status}`
* Los administradores del sistema deben conocer la siguiente alternativa:

   `/sbin/service ImageServing {start|stop|status}`
