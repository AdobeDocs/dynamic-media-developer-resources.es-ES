---
description: Todos los archivos de registro se escriben en la misma carpeta de registro especificada con el directorio TC.
solution: Experience Manager
title: Registro del servidor
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---


# Registro del servidor{#server-logging}

Todos los archivos de registro se escriben en la misma carpeta de registro especificada con TC::directory.

Los archivos de registro suelen crearse y rotarse diariamente. Los archivos de registro anteriores de la carpeta de registro se eliminan automáticamente después de un número especificado de días ( `TC::maxDays`).

Importante Debe reservarse una cantidad suficiente de espacio en disco para los archivos de registro a fin de evitar que se agote el espacio en disco. Es posible que se requieran de 1 a 2 GB/día para un servidor que se utiliza con frecuencia y para la configuración de registro predeterminada.

Platform Server y Image Server crean los tres tipos de archivos de registro que se describen a continuación.

Otros componentes de servicio de imágenes y algunos otros paquetes de Dynamic Media, como los visores de Dynamic Media, también pueden crear archivos de registro en la misma carpeta. Estos archivos de registro son para uso interno de Dynamic Media y pueden ser solicitados por el soporte técnico de Dynamic Media para resolución de problemas.

* [Registro de acceso](c-access-log.md)
* [Registro de seguimiento](c-trace-log.md)
* [Registro del servidor de imágenes](c-image-server-log.md)

## Véase también {#section-5ff5e46031b1461c92de24e632610d6d}

[Registro](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f) de acceso, registro de  [depuración/seguimiento](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
