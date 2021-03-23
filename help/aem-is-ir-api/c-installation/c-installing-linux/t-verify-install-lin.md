---
description: Después de instalar Image Serving en Linux, verifique la instalación.
seo-description: Después de instalar Image Serving en Linux, verifique la instalación.
seo-title: Verificación de la instalación
solution: Experience Manager
title: Verificación de la instalación
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# Verificación de la instalación{#verifying-the-installation}

Después de instalar Image Serving en Linux, verifique la instalación.

Image Server está instalado como un demonio Linux.

**Para verificar la instalación**

1. Compruebe que el servicio de imágenes está configurado para iniciarse automáticamente y que se está ejecutando:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Debe tener permisos raíz para ejecutar estas secuencias de comandos.

1. Abra un explorador de Internet en el mismo host o en otro diferente y compruebe las respuestas predeterminadas del servidor:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

En las respuestas, compruebe la presencia de elementos que empiecen por &quot; `imageServer.`&quot;, lo que indica que Platform Server podría comunicarse correctamente con el servidor de imágenes.
>Se puede realizar una verificación adicional utilizando las páginas de muestra de los paquetes de documentación y demostración, si están instalados.

