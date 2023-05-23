---
description: Todos los archivos de registro se escriben en la misma carpeta de registro especificada con el directorio TC.
solution: Experience Manager
title: Registro de servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# Registro de servidor{#server-logging}

Todos los archivos de registro se escriben en la misma carpeta de registro especificada con TC::directory.

Los archivos de registro se suelen crear y rotar diariamente. Los archivos de registro más antiguos de la carpeta de registro se eliminan automáticamente después de un número determinado de días ( `TC::maxDays`).

Importante Se debe reservar una cantidad suficiente de espacio en disco para los archivos de registro a fin de evitar que se agote el espacio en disco. Es posible que se necesite de 1 a 2 GB/día para un servidor muy utilizado y la configuración de registro predeterminada.

El [!DNL Platform Server] y el servidor de imágenes crean los tres tipos de archivos de registro que se describen a continuación.

Otros componentes del servicio de imágenes y ciertos paquetes de Dynamic Media, como los visores de Dynamic Media, también pueden crear archivos de registro en la misma carpeta. Estos archivos de registro son para uso interno de Dynamic Media y el servicio de asistencia técnica de Dynamic Media los puede solicitar para solucionar problemas.

* [Registro de acceso](c-access-log.md)
* [Registro de seguimiento](c-trace-log.md)
* [Registro de Image Server](c-image-server-log.md)

## Véase también {#section-5ff5e46031b1461c92de24e632610d6d}

[Registro de acceso](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [Depuración/Seguimiento del registro](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
