---
description: Utilice esta configuración del servidor para redirigir los errores.
seo-description: Utilice esta configuración del servidor para redirigir los errores.
seo-title: Redirección de errores
solution: Experience Manager
title: Redirección de errores
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Redirección de errores{#error-redirection}

Utilice esta configuración del servidor para redirigir los errores.

>[!NOTE]
>
>Los caracteres de tubería (|) en la ruta de acceso de red no son compatibles para la redirección de errores.

## PS::errorRedirect.rootUrl - Servidor de redireccionamiento {#section-85f22e48d68842a490b0e1191543b558}

La dirección URL raíz ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) para la implementación secundaria del servicio de imágenes a la que se deben redirigir las solicitudes que fallan localmente. La redirección de errores está deshabilitada (predeterminada) cuando esta configuración está vacía o no está definida.

## PS::errorRedirect.connectTimeout - Tiempo de espera de conexión de redireccionamiento {#section-3971be8f720d4b32a2cc7860b4085971}

Tiempo máximo (en ms) que el servidor esperará a que se establezca una conexión con el servidor secundario antes de devolver un error al cliente.

## PS::errorRedirect.socketTimeout - Tiempo de espera de respuesta de redireccionamiento {#section-69d8579f748d4044bca99dfb64dd523c}

Tiempo máximo (en ms) que el servidor esperará para que el servidor secundario devuelva datos antes de abandonar la solicitud de redirección y devolver un error al cliente.
