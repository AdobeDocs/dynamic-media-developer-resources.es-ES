---
description: Después de instalar Dynamic Media Image Serving, debe verificar la instalación.
solution: Experience Manager
title: Verificación de la instalación
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Verificación de la instalación{#verifying-the-installation}

Después de instalar Dynamic Media Image Serving, debe verificar la instalación.

Image Server está instalado como un servicio de Windows.

1. Abra el Panel de control de Campaign Servicios y compruebe que &quot;Dynamic Media Image Serving&quot; esté presente con el estado &quot;Started&quot; (Inicio).
1. Abra un explorador de Internet en el mismo host o en otro diferente y compruebe las respuestas predeterminadas del servidor:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Compruebe la presencia de elementos &quot; `imageServer.`&quot; en la respuesta, lo que indica que el servidor de imágenes está escuchando.
>Se puede realizar una verificación adicional utilizando las páginas de muestra de los paquetes de documentación y demostración, si están instalados.

