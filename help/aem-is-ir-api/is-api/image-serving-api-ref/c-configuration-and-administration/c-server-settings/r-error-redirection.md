---
description: Utilice esta configuración del servidor para redirigir los errores.
solution: Experience Manager
title: Redirección de errores
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Redirección de errores{#error-redirection}

Utilice esta configuración del servidor para redirigir los errores.

>[!NOTE]
>
>Los caracteres de tubería (|) en la ruta de acceso neta no son compatibles con la redirección de errores.

## PS::errorRedirect.rootUrl - Servidor de redireccionamiento {#section-85f22e48d68842a490b0e1191543b558}

La URL raíz ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]] para la implementación secundaria de Image Serving a la que se deben redirigir las solicitudes que fallan localmente. El redireccionamiento de errores está desactivado (predeterminado) cuando esta configuración está vacía o no está definida.

## PS::errorRedirect.connectTimeout - Tiempo de espera de conexión de redireccionamiento {#section-3971be8f720d4b32a2cc7860b4085971}

Tiempo máximo (en ms) que el servidor esperará a que se establezca una conexión con el servidor secundario antes de devolver un error al cliente.

## PS::errorRedirect.socketTimeout - Tiempo de espera de respuesta de redireccionamiento {#section-69d8579f748d4044bca99dfb64dd523c}

Tiempo máximo (en ms) que el servidor esperará para que el servidor secundario devuelva datos antes de abandonar la solicitud de redirección y devolver un error al cliente.
