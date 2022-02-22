---
title: Verificación de la instalación
description: Después de instalar Dynamic Media Image Serving, debe verificar la instalación.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Verificación de la instalación {#verifying-the-installation}

Después de instalar Dynamic Media Image Serving, debe verificar la instalación.

Image Server está instalado como un servicio de Windows.

1. Abra el Panel de control de Campaign Servicios y compruebe que `Dynamic Media Image Serving` está presente con un estado de `Started`.
1. Abra un explorador de Internet en el mismo host o en otro diferente y compruebe las respuestas predeterminadas del servidor:

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

Compruebe la presencia de &quot; `imageServer.`&quot; elementos en la respuesta, que indican que el Servidor de imágenes está escuchando.
>Se puede realizar una verificación adicional utilizando las páginas de muestra de los paquetes de documentación y demostración, si están instalados.
