---
title: Iniciar o detener en Linux®
description: Existen dos opciones para iniciar o detener el servicio de imágenes en Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Iniciar o detener en Linux® {#starting-or-stopping-on-linux}

Existen dos opciones para iniciar o detener el servicio de imágenes en Linux®.

* El script para verificar el estado del servicio de imágenes o para iniciar y detener el servicio de imágenes se encuentra en la carpeta [!DNL ImageServing/bin]:

  `ImageServing.sh {start|stop|restart|status}`
* La siguiente alternativa debería resultarles familiar a los administradores del sistema:

  `/sbin/service ImageServing {start|stop|status}`
