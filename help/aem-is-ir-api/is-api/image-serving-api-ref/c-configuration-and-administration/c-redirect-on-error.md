---
description: Los servidores IS se pueden configurar para que conmuten por error a servidores alternativos en las solicitudes que impliquen una imagen de origen que no se pueda abrir o leer correctamente.
solution: Experience Manager
title: Redirigir por error
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
TQID: 'https://experienceleague.adobe.com/jNvJP4nJ7W1thf-ZDbSCzry54H8wI4DVGK8FW6koNCw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# Redirigir por error{#redirect-on-error}

Los servidores IS se pueden configurar para que conmuten por error a servidores alternativos en las solicitudes que impliquen una imagen de origen que no se pueda abrir o leer correctamente.

Se redirigen los siguientes tipos de solicitudes:

* Imágenes IS que están en el catálogo, pero no en el disco.

  Si una imagen no está en un catálogo, no se debe producir un redireccionamiento de error cuando no se pueda encontrar la imagen.

* Imágenes, perfiles de color o fuentes dañados.
* No se puede encontrar el contenido estático en el disco.

  Las solicitudes de contenido estático se redirigen cuando no se pueden encontrar en el disco, aunque el contenido estático al que se hace referencia no tenga un registro de catálogo.

La redirección de errores no se produce en ningún otro caso.

Cuando está habilitado y se produce un error de este tipo durante el procesamiento de la solicitud, el servidor principal envía la solicitud al servidor secundario para que la procese. La respuesta, independientemente de si indica éxito o error, se reenvía directamente al cliente. El servidor principal marca las entradas de registro de dichas solicitudes reenviadas con caché para utilizar `REMOTE`. El servidor principal no almacena en caché localmente los datos de respuesta.

El redireccionamiento de errores está habilitado al establecer `PS::errorRedirect.rootUrl` en el nombre de dominio HTTP y el número de puerto del servidor secundario. Además, el tiempo de espera de conexión se configura con `PS::errorRedirect.connectTimeout` y el tiempo máximo que el servidor principal espera una respuesta del servidor secundario antes de devolver un error al cliente se configura con `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Si no se puede establecer contacto con el servidor secundario, se devuelve una respuesta de error de texto al cliente, incluso si se ha configurado una imagen predeterminada o una imagen de error.

>[!NOTE]
>
>No se admiten los caracteres de barra vertical (|) en la ruta de acceso de red para la redirección de errores.

## Véase también {#section-2e8bfc128b944baf8108279d16492f3f}

[Redirección de errores](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
