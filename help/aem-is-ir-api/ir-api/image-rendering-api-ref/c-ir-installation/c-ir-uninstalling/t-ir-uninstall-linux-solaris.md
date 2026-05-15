---
title: Desinstalación en Linux® y Solaris™
description: Siga estas instrucciones para desinstalar Image Rendering en un sistema Linux® o Solaris™.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
TQID: 'https://experienceleague.adobe.com/RmD5z5300Nw12kSsOretyAl5p-TeFkox-Cyqm1MrF5w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# Desinstalación en Linux® y Solaris™{#uninstalling-on-linux-and-solaris}

Siga estas instrucciones para desinstalar Image Rendering en un sistema Linux® o Solaris™. Existen dos métodos diferentes que puede utilizar. Realice una de las siguientes acciones:

## Método 1

1. Buscar [!DNL uninstall.sh].

   Se encuentra en el directorio desde el que se instaló ImageRendering. Si se ha quitado este directorio, debe descomprimir y descomprimir el paquete de instalación original para extraer [!DNL uninstall.sh].
1. Ejecute [!DNL uninstall.sh] y siga las instrucciones que aparecen en pantalla.

## Método 2

1. Detenga ImageRendering con lo siguiente:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. Elimine ImageRendering de su sistema. El comando que utilice depende del sistema.
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. Elimine los directorios o archivos que no se eliminaron en el paso 2.

