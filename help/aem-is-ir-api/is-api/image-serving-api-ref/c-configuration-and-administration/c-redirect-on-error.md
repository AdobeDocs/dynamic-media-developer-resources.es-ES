---
description: Los servidores IS pueden configurarse para conmutar por error a servidores alternativos en el caso de solicitudes que impliquen una imagen de origen que no se pueda abrir ni leer correctamente.
seo-description: Los servidores IS pueden configurarse para conmutar por error a servidores alternativos en el caso de solicitudes que impliquen una imagen de origen que no se pueda abrir ni leer correctamente.
seo-title: Redirigir en caso de error
solution: Experience Manager
title: Redirigir en caso de error
uuid: 894babe9-9c3c-4972-ae8f-387d65b4167d
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# Redireccionar en caso de error{#redirect-on-error}

Los servidores IS pueden configurarse para conmutar por error a servidores alternativos en el caso de solicitudes que impliquen una imagen de origen que no se pueda abrir ni leer correctamente.

Se redirigen los siguientes tipos de solicitudes:

* Imágenes IS que están en el catálogo, pero no en el disco.

   Si una imagen no está en un catálogo, el redireccionamiento de errores no debería ocurrir cuando no se encuentra la imagen.

* Imágenes dañadas, perfiles de color o fuentes.
* No se puede encontrar contenido estático en el disco.

   Las solicitudes de contenido estático se redirigen cuando no se pueden encontrar en el disco, aunque el contenido estático al que se hace referencia no tenga un registro de catálogo.

El redireccionamiento de errores no se producirá en ningún otro caso.

Cuando se habilita y se produce un error de este tipo durante el procesamiento de la solicitud, el servidor principal envía la solicitud al servidor secundario para que la procese. La respuesta, independientemente de si indica que se ha realizado correctamente o no, se reenvía directamente al cliente. El servidor principal marca las entradas de registro de dichas solicitudes reenviadas con el uso de caché `REMOTE`. El servidor principal no almacena en caché localmente los datos de respuesta.

El redireccionamiento de errores está habilitado al establecer `PS::errorRedirect.rootUrl` en el nombre de dominio HTTP y número de puerto del servidor secundario. Además, el tiempo de espera de la conexión se configura con `PS::errorRedirect.connectTimeout` y el tiempo máximo que el servidor principal esperará una respuesta del servidor secundario antes de devolver un error al cliente se configura con `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Si no se puede establecer contacto con el servidor secundario, se devolverá al cliente una respuesta de error de texto, incluso si se ha configurado una imagen o imagen de error predeterminada.

>[!NOTE]
>
>Los caracteres de tubería (|) en la ruta de acceso neta no son compatibles con la redirección de errores.

## Véase también {#section-2e8bfc128b944baf8108279d16492f3f}

[Redirección de errores](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
