---
description: Después de instalar Dynamic Media Image Serving, debe verificar la instalación.
seo-description: Después de instalar Dynamic Media Image Serving, debe verificar la instalación.
seo-title: Verificación de la instalación
solution: Experience Manager
title: Verificación de la instalación
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
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

