---
description: Después de instalar Dynamic Media Image Serving, debe verificar la instalación.
solution: Experience Manager
title: Verificación de la instalación
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '118'
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
