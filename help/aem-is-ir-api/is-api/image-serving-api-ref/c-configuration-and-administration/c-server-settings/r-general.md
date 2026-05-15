---
description: Configuración general del servidor
solution: Experience Manager
title: General
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
TQID: 'https://experienceleague.adobe.com/hjww7EYpf4xNxpUFQ1fudMOqNtokgykthwhonn78ZFE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# General{#general}

Configuración general del servidor

## TC::PsPort: puerto de escucha principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Especifica el puerto de escucha principal de [!DNL Platform Server]. Este puerto también se utiliza para acceder a la documentación y a las páginas de ejemplo del servicio de imágenes, el procesamiento de imágenes y los visualizadores de Dynamic Media (si están instalados).

## IS::CacheServerUrl: URL raíz del servicio de almacenamiento en caché {#section-bcca227a1f91453b834db4ea050968e2}

Especifica la ruta raíz HTTP para permitir que el servidor de imágenes acceda al servicio de almacenamiento en caché. Debe establecerse en [!DNL http://localhost:TC::PsPort /is/cache/secondary], con el número de puerto que coincida con `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration: TTL predeterminado de Image Source remoto {#section-e4c31228b459492cacd2f482d9575f71}

El TTL para imágenes en caché obtenidas mediante HTTP desde un origen remoto usando la construcción `src={…}`. Solo se utiliza cuando el servidor remoto no incluye un encabezado Caducidad en su respuesta HTTP. Valor entero en segundos.

## IS::RemoteUrlTimeout: tiempo de espera de Image Source remoto {#section-437646c479cc4bea81dae42100a3c50a}

El tiempo que el servidor de imágenes espera a que un servidor remoto envíe el archivo de imagen solicitado a través de HTTP antes de devolver un error. Valor entero en segundos.

## PS::allowDefaultCatalogRequests: habilitar/deshabilitar solicitudes de catálogo predeterminadas {#section-484e442a115a49b4ac269d1718b351e1}

Establezca el valor en False para no permitir solicitudes que no incluyan un ID de catálogo válido en la ruta. El valor predeterminado es `true`. Cuando se establece en `false`, se devuelve un error para las solicitudes sin un ID de catálogo.

>[!NOTE]
>
>`req=catalogprops` no está sujeto a esta configuración.

## PS::saveToFile.saveTimeout: tiempo de espera para guardar archivos {#section-d22afd8ad86144b28684ed95a59db40e}

Valor de tiempo de espera predeterminado para `req=saveToFile` cuando no se especifica `timeout=`. `msec`. Se devuelve un error si la operación de guardado no se completa en el período de tiempo especificado.
