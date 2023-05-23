---
description: Utilice esta configuración del servidor para redirigir errores.
solution: Experience Manager
title: Error de redirección
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# Error de redirección{#error-redirection}

Utilice esta configuración del servidor para redirigir errores.

>[!NOTE]
>
>No se admiten los caracteres de barra vertical (|) en la ruta de acceso de red para la redirección de errores.

## PS::errorRedirect.rootUrl - Servidor de redireccionamiento {#section-85f22e48d68842a490b0e1191543b558}

La URL raíz ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]]) para la implementación secundaria del servicio de imágenes a la que se deben redirigir las solicitudes que fallan localmente. La redirección de errores está deshabilitada (predeterminada) cuando esta configuración está vacía o no está definida.

## PS::errorRedirect.connectTimeout: tiempo de espera de conexión de redireccionamiento {#section-3971be8f720d4b32a2cc7860b4085971}

Tiempo máximo (en ms) que el servidor esperará a que se establezca una conexión con el servidor secundario antes de devolver un error al cliente.

## PS::errorRedirect.socketTimeout: tiempo de espera de respuesta de redireccionamiento {#section-69d8579f748d4044bca99dfb64dd523c}

Tiempo máximo (en ms) que el servidor esperará a que el servidor secundario devuelva datos antes de abandonar la solicitud de redirección y devolver un error al cliente.
