---
description: Todos los archivos de registro se escriben en la misma carpeta de registro especificada con el directorio TC.
solution: Experience Manager
title: Registro de servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
TQID: 'https://experienceleague.adobe.com/9I1gAXWb1Rpuml9WCCVPVC7FrpVazWN79Sk0-bb-tDc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 1%

---

# Registro de servidor{#server-logging}

Todos los archivos de registro se escriben en la misma carpeta de registro especificada con TC::directory.

Los archivos de registro se suelen crear y rotar diariamente. Los archivos de registro más antiguos de la carpeta de registro se eliminarán automáticamente después de un número determinado de días ( `TC::maxDays`).

Importante Se debe reservar una cantidad suficiente de espacio en disco para los archivos de registro a fin de evitar que se agote el espacio en disco. Es posible que se necesite de 1 a 2 GB/día para un servidor muy utilizado y la configuración de registro predeterminada.

[!DNL Platform Server] y el servidor de imágenes crean los tres tipos de archivos de registro que se describen a continuación.

Otros componentes del servicio de imágenes y ciertos paquetes de Dynamic Media, como los visores de Dynamic Media, también pueden crear archivos de registro en la misma carpeta. Estos archivos de registro son para uso interno de Dynamic Media y el servicio de asistencia técnica de Dynamic Media los puede solicitar para solucionar problemas.

* [Registro de acceso](c-access-log.md)
* [Registro de seguimiento](c-trace-log.md)
* [Registro de Image Server](c-image-server-log.md)

## Véase también {#section-5ff5e46031b1461c92de24e632610d6d}

[Registro de acceso](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [Registro de depuración/seguimiento](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
