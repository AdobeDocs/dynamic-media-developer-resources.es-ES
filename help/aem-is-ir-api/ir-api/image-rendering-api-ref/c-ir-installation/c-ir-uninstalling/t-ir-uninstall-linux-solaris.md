---
description: Siga estas instrucciones para desinstalar Image Rendering en un sistema Linux o Solaris.
seo-description: Siga estas instrucciones para desinstalar Image Rendering en un sistema Linux o Solaris.
seo-title: Desinstalación en Linux y Solaris
solution: Experience Manager
title: Desinstalación en Linux y Solaris
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# Desinstalación en Linux y Solaris{#uninstalling-on-linux-and-solaris}

Siga estas instrucciones para desinstalar Image Rendering en un sistema Linux o Solaris.

Existen dos maneras de desinstalar Image Rendering en un sistema Linux o Solaris.

**Método 1**

1. Buscar [!DNL uninstall.sh].

   Se encuentra en el directorio desde el que se instaló ImageRendering. Si se ha eliminado este directorio, el paquete de instalación original debe descomprimirse y descomprimirse para extraer [!DNL uninstall.sh].
1. Ejecute [!DNL uninstall.sh] y siga las instrucciones que aparecen en la pantalla.

>**Método 2**
>
>1. Detener ImageRendering con: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Elimine ImageRendering de su sistema.

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



