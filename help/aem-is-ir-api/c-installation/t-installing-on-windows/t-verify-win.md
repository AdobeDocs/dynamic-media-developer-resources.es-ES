---
title: Verificación de la instalación
description: Después de instalar el servicio de imágenes de Dynamic Media, debe comprobar la instalación.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
TQID: 'https://experienceleague.adobe.com/2i1-Ncy7lyIbm8BHFZGVLNIDnZUOA9sr3tZ970WswL4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# Verificación de la instalación {#verifying-the-installation}

Después de instalar el servicio de imágenes de Dynamic Media, debe comprobar la instalación.

El servidor de imágenes está instalado como servicio de Windows.

1. Abra el Panel de control de Campaign Servicios y compruebe que `Dynamic Media Image Serving` se encuentra presente con el estado `Started`.
1. Abra un explorador de Internet en el mismo host o en otro distinto y compruebe las respuestas predeterminadas del servidor:

   `http:// server:port /is/image`

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

Compruebe la presencia de &quot;`imageServer.`&quot; elementos en la respuesta, lo que indica que el servidor de imágenes está escuchando.

>Se puede realizar una verificación adicional utilizando las páginas de muestra de los paquetes de documentación y demostración, si están instalados.
