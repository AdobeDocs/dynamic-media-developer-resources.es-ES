---
description: Configuración general del servidor
solution: Experience Manager
title: General
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# General{#general}

Configuración general del servidor

## TC::PsPort - Puerto principal de escucha {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Especifica el puerto de escucha principal de Platform Server. Este puerto también se utiliza para acceder a la documentación y a las páginas de ejemplo de Image Serving, Image Rendering y Dynamic Media Viewers (si están instalados).

## IS::CacheServerUrl - Url Raíz Del Servicio De Almacenamiento En Caché {#section-bcca227a1f91453b834db4ea050968e2}

Especifica la ruta raíz HTTP para permitir el acceso del servidor de imágenes al servicio de almacenamiento en caché. Debe establecerse en [!DNL http://localhost:TC::PsPort /is/cache/secondary], con el número de puerto coincidente `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL predeterminado de Image Source remoto {#section-e4c31228b459492cacd2f482d9575f71}

El TTL para imágenes en caché obtenidas mediante HTTP desde un origen remoto mediante la construcción `src={…}`. Solo se utiliza cuando el servidor remoto no incluye un encabezado Caducidad en su respuesta HTTP. Valor entero en segundos.

## IS::RemoteUrlTimeout - Tiempo de espera de Image Source remoto {#section-437646c479cc4bea81dae42100a3c50a}

El tiempo que el servidor de imágenes esperará para que un servidor remoto entregue el archivo de imagen solicitado mediante HTTP antes de devolver un error. Valor entero en segundos.

## PS::allowDefaultCatalogRequests - Habilitar/deshabilitar solicitudes de catálogo predeterminadas {#section-484e442a115a49b4ac269d1718b351e1}

Configúrelo en falso para no permitir solicitudes que no incluyan un id de catálogo válido en la ruta. El valor predeterminado es `true`. Cuando se establece en `false`, se devuelve un error para las solicitudes sin un id de catálogo.

>[!NOTE]
>
>`req=catalogprops` no está sujeto a esta configuración.

## PS::saveToFile.saveTimeout: tiempo de espera de almacenamiento del archivo {#section-d22afd8ad86144b28684ed95a59db40e}

Valor de tiempo de espera predeterminado para `req=saveToFile` cuando `timeout=`no se especifica. `msec`. Se devolverá un error si la operación de guardado no se completa en el plazo especificado.
