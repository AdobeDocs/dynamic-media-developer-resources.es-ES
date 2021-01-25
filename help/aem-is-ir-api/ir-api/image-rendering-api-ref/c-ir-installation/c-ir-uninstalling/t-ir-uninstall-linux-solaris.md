---
description: Siga estas instrucciones para desinstalar el procesamiento de imágenes en un sistema Linux o Solaris.
seo-description: Siga estas instrucciones para desinstalar el procesamiento de imágenes en un sistema Linux o Solaris.
seo-title: Desinstalación en Linux y Solaris
solution: Experience Manager
title: Desinstalación en Linux y Solaris
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Desinstalación en Linux y Solaris{#uninstalling-on-linux-and-solaris}

Siga estas instrucciones para desinstalar el procesamiento de imágenes en un sistema Linux o Solaris.

Existen dos formas de desinstalar el procesamiento de imágenes en un sistema Linux o Solaris.

**Método 1**

1. Buscar [!DNL uninstall.sh].

   Se encuentra en el directorio desde el que se instaló ImageRendering. Si se ha eliminado este directorio, el paquete de instalación original debe descomprimirse y no rastrearse para extraer [!DNL uninstall.sh].
1. Ejecute [!DNL uninstall.sh] y siga las instrucciones que aparecen en la pantalla.

>**Método 2**
>
>1. Detener procesamiento de imágenes con: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Elimine ImageRendering del sistema.

>
>   
El comando para quitar ImageRendering depende del sistema:
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. Elimine los directorios o archivos que no se hayan eliminado en el paso 2.

>



