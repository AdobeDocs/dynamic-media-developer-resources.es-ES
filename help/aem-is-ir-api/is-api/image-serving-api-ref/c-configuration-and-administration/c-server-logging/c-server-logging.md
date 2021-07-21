---
description: Todos los archivos de registro se escriben en la misma carpeta de registro especificada con el directorio TC.
solution: Experience Manager
title: Registro del servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# Registro del servidor{#server-logging}

Todos los archivos de registro se escriben en la misma carpeta de registro especificada con TC::directory.

Los archivos de registro suelen crearse y girarse diariamente. Los archivos de registro más antiguos de la carpeta de registro se eliminan automáticamente después de un número especificado de días ( `TC::maxDays`).

Importante Se debe reservar una cantidad suficiente de espacio en disco para los archivos de registro a fin de evitar quedarse sin espacio en disco. Es posible que se requieran de 1 a 2 GB/día para un servidor muy utilizado y la configuración de registro predeterminada.

Platform Server y Image Server crean los tres tipos de archivos de registro que se describen a continuación.

Otros componentes de servicio de imágenes y algunos otros paquetes de Dynamic Media, como los visores de Dynamic Media, también pueden crear archivos de registro en la misma carpeta. Estos archivos de registro son para uso interno de Dynamic Media y el soporte técnico de Dynamic Media puede solicitarlos para solucionar problemas.

* [Registro de acceso](c-access-log.md)
* [Registro de seguimiento](c-trace-log.md)
* [Registro del servidor de imágenes](c-image-server-log.md)

## Véase también {#section-5ff5e46031b1461c92de24e632610d6d}

[Registro](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f) de acceso, registro de  [depuración/seguimiento](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
