---
title: Verificación de la instalación
description: Después de instalar Image Serving en Linux®, verifique la instalación.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# Verificación de la instalación{#verifying-the-installation}

Después de instalar Image Serving en Linux®, verifique la instalación.

Image Server está instalado como un demonio Linux®.

**Para verificar la instalación**

1. Compruebe que el servicio de imágenes está configurado para iniciarse automáticamente y que se está ejecutando:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Debe tener permisos raíz para ejecutar estas secuencias de comandos.

1. Abra un explorador de Internet en el mismo host o en otro diferente y compruebe las respuestas predeterminadas del servidor:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

En las respuestas, compruebe la presencia de elementos que empiecen por `imageServer`, que indican que Platform Server podría comunicarse correctamente con el Image Server.

>Se puede realizar una verificación adicional utilizando las páginas de muestra de los paquetes de documentación y demostración, si están instalados.
