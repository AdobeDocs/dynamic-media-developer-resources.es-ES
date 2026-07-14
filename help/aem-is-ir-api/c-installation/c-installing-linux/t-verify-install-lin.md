---
title: Verificación de la instalación
description: Después de instalar Image Serving en Linux®, verifique la instalación.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
TQID: 'https://experienceleague.adobe.com/LyHlwiFL1b-iwo1kSnUeNfNo3fZY6FZetHgnNFoxGZo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 118
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

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

En las respuestas, compruebe la presencia de elementos que empiecen por `imageServer`, lo que indica que [!DNL Platform Server] se pudo comunicar correctamente con el servidor de imágenes.

>Se puede realizar una verificación adicional utilizando las páginas de muestra de los paquetes de documentación y demostración, si están instalados.

