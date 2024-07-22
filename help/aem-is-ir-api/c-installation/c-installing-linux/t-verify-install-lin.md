---
title: Verificación de la instalación
description: Después de instalar Image Serving en Linux®, verifique la instalación.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Verificación de la instalación{#verifying-the-installation}

Después de instalar Image Serving en Linux®, verifique la instalación.

El servidor de imágenes está instalado como daemon de Linux®.

**Para comprobar la instalación**

1. Compruebe que el servicio de imágenes esté configurado para iniciarse automáticamente y que se esté ejecutando:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Debe tener permisos de raíz para ejecutar estas secuencias de comandos.

1. Abra un explorador de Internet en el mismo host o en otro distinto y compruebe las respuestas predeterminadas del servidor:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

En las respuestas, compruebe la presencia de elementos que empiecen por `imageServer`, lo que indica que [!DNL Platform Server] se pudo comunicar correctamente con el servidor de imágenes.

>Se puede realizar una verificación adicional utilizando las páginas de muestra de los paquetes de documentación y demostración, si están instalados.
