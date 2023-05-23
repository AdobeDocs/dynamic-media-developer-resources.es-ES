---
title: Desinstalación en Linux® y Solaris™
description: Siga estas instrucciones para desinstalar Image Rendering en un sistema Linux® o Solaris™.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 5%

---

# Desinstalación en Linux® y Solaris™{#uninstalling-on-linux-and-solaris}

Siga estas instrucciones para desinstalar Image Rendering en un sistema Linux® o Solaris™. Existen dos métodos diferentes que puede utilizar. Realice una de las siguientes acciones:

## Método 1

1. Buscar [!DNL uninstall.sh].

   Se encuentra en el directorio desde el que se instaló ImageRendering. Si se ha eliminado este directorio, el paquete de instalación original debe descomprimirse y descomprimirse para poder extraerlo [!DNL uninstall.sh].
1. Ejecutar [!DNL uninstall.sh] y siga las instrucciones que aparecen en pantalla.

## Método 2

1. Detenga ImageRendering con lo siguiente:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. Elimine ImageRendering de su sistema. El comando que utilice depende del sistema.
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. Elimine los directorios o archivos que no se eliminaron en el paso 2.

