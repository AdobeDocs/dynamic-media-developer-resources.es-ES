---
description: Después de instalar el servicio de imágenes en Linux, verifique la instalación.
seo-description: Después de instalar el servicio de imágenes en Linux, verifique la instalación.
seo-title: Verificación de la instalación
solution: Experience Manager
title: Verificación de la instalación
topic: Scene7 Image Serving - Image Rendering API
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---


# Verificación de la instalación{#verifying-the-installation}

Después de instalar el servicio de imágenes en Linux, verifique la instalación.

Image Server se instala como un demonio Linux.

**Para verificar la instalación**

1. Compruebe que el servicio de imágenes está configurado para el inicio automáticamente y que se está ejecutando:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Debe tener permisos de raíz para ejecutar estas secuencias de comandos.

1. Abra un explorador de Internet en el mismo host o en otro diferente y compruebe las respuestas predeterminadas del servidor:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/procesar]

En las respuestas, compruebe la presencia de elementos que empiecen por &quot; `imageServer.`&quot;, lo que indica que el Servidor de plataforma podría comunicarse correctamente con el Servidor de imágenes.
>Se puede realizar una verificación adicional utilizando las páginas de muestra de los paquetes Documentación y Demostración, si están instalados.

