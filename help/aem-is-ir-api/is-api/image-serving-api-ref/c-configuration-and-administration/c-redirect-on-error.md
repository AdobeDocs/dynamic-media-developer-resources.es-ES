---
description: Los servidores IS pueden configurarse para conmutar por error a servidores alternativos las solicitudes que impliquen una imagen de origen que no se pueda abrir o leer correctamente.
seo-description: Los servidores IS pueden configurarse para conmutar por error a servidores alternativos las solicitudes que impliquen una imagen de origen que no se pueda abrir o leer correctamente.
seo-title: Redireccionamiento por error
solution: Experience Manager
title: Redireccionamiento por error
topic: Scene7 Image Serving - Image Rendering API
uuid: 894babe9-9c3c-4972-ae8f-387d65b4167d
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---


# Redireccionamiento por error{#redirect-on-error}

Los servidores IS pueden configurarse para conmutar por error a servidores alternativos las solicitudes que impliquen una imagen de origen que no se pueda abrir o leer correctamente.

Se redirigen los siguientes tipos de solicitudes:

* Imágenes IS que están en el catálogo pero no en el disco.

   Si una imagen no está en un catálogo, la redirección de errores no debe producirse cuando no se encuentra la imagen.

* Imágenes, perfiles de color o fuentes dañadas.
* No se puede encontrar contenido estático en el disco.

   Las solicitudes de contenido estático se redirigen cuando no se pueden encontrar en el disco, aunque el contenido estático al que se hace referencia no tenga un registro de catálogo.

La redirección de errores no se producirá en ningún otro caso.

Cuando se habilita y se produce un error de este tipo durante el procesamiento de la solicitud, el servidor primario enviará la solicitud al servidor secundario para su procesamiento. La respuesta, independientemente de si indica éxito o fracaso, se reenvía directamente al cliente. El servidor principal marca las entradas de registro de dichas solicitudes reenviadas con el uso de la caché `REMOTE`. El servidor primario no almacena en caché localmente los datos de respuesta.

La redirección de errores se habilita al establecer `PS::errorRedirect.rootUrl` el nombre de dominio HTTP y el número de puerto del servidor secundario. Además, el tiempo de espera de conexión se configura con `PS::errorRedirect.connectTimeout` y el tiempo máximo que el servidor primario espera una respuesta del servidor secundario antes de devolver un error al cliente se configura con `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Si no se puede establecer contacto con el servidor secundario, se devolverá al cliente una respuesta de error de texto, aunque se haya configurado una imagen o imagen de error predeterminada.

>[!NOTE]
>
>Los caracteres de tubería (|) en la ruta de acceso de red no son compatibles para la redirección de errores.

## Véase también {#section-2e8bfc128b944baf8108279d16492f3f}

[Redirección de errores](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
