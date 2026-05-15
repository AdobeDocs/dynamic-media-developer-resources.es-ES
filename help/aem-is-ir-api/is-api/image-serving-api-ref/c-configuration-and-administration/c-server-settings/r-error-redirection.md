---
description: Utilice esta configuración del servidor para redirigir errores.
solution: Experience Manager
title: Error de redirección
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
TQID: 'https://experienceleague.adobe.com/3fcob7pfE-bMms-4PtD5MKkcolKHmXEWdzEL7vgzLhc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# Error de redirección{#error-redirection}

Utilice esta configuración del servidor para redirigir errores.

>[!NOTE]
>
>No se admiten los caracteres de barra vertical (|) en la ruta de acceso de red para la redirección de errores.

## PS::errorRedirect.rootUrl - Servidor de redireccionamiento {#section-85f22e48d68842a490b0e1191543b558}

Dirección URL raíz ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) de la implementación secundaria del servicio de imágenes a la que se deben redirigir las solicitudes con error local. La redirección de errores está deshabilitada (predeterminada) cuando esta configuración está vacía o no está definida.

## PS::errorRedirect.connectTimeout: tiempo de espera de conexión de redireccionamiento {#section-3971be8f720d4b32a2cc7860b4085971}

Tiempo máximo (en milisegundos) que el servidor espera a que se establezca una conexión con el servidor secundario antes de devolver un error al cliente.

## PS::errorRedirect.socketTimeout: tiempo de espera de respuesta de redireccionamiento {#section-69d8579f748d4044bca99dfb64dd523c}

Tiempo máximo (en ms) que el servidor espera a que el servidor secundario devuelva datos antes de abandonar la solicitud de redirección y devolver un error al cliente.
