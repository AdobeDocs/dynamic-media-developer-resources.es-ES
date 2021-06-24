---
description: Existen dos opciones para iniciar o detener Image Serving en Linux.
solution: Experience Manager
title: Inicio o parada en Linux
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Inicio o parada en Linux{#starting-or-stopping-on-linux}

Existen dos opciones para iniciar o detener Image Serving en Linux.

* La secuencia de comandos para iniciar, detener y verificar el estado de Image Serving se encuentra en la carpeta [!DNL ImageServing/bin]:

   `ImageServing.sh {start|stop|restart|status}`
* La siguiente alternativa debería resultarle familiar a los administradores del sistema:

   `/sbin/service ImageServing {start|stop|status}`
