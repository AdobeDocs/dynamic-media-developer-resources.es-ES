---
description: Los servidores IS se pueden configurar para que conmuten por error a servidores alternativos en las solicitudes que impliquen una imagen de origen que no se pueda abrir o leer correctamente.
solution: Experience Manager
title: Redirigir por error
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
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

Cuando está habilitado y se produce un error de este tipo durante el procesamiento de la solicitud, el servidor principal envía la solicitud al servidor secundario para que la procese. La respuesta, independientemente de si indica éxito o error, se reenvía directamente al cliente. El servidor principal marca las entradas de registro de dichas solicitudes reenviadas con el uso de caché `REMOTE`. El servidor principal no almacena en caché localmente los datos de respuesta.

La redirección de errores está habilitada mediante la configuración `PS::errorRedirect.rootUrl` al nombre de dominio HTTP y al número de puerto del servidor secundario. Además, el tiempo de espera de conexión se configura con `PS::errorRedirect.connectTimeout` y el tiempo máximo que el servidor principal espera una respuesta del servidor secundario antes de devolver un error al cliente se configura con `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Si no se puede establecer contacto con el servidor secundario, se devuelve una respuesta de error de texto al cliente, incluso si se ha configurado una imagen predeterminada o una imagen de error.

>[!NOTE]
>
>No se admiten los caracteres de barra vertical (|) en la ruta de acceso de red para la redirección de errores.

## Véase también {#section-2e8bfc128b944baf8108279d16492f3f}

[Redirección de errores](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
