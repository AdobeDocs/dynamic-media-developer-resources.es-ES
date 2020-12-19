---
description: Configuración general del servidor
seo-description: Configuración general del servidor
seo-title: General
solution: Experience Manager
title: General
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 2%

---


# General{#general}

Configuración general del servidor

## TC::PsPort - Puerto de escucha principal {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Especifica el puerto de escucha principal para el servidor de plataforma. Este puerto también se utiliza para acceder a la documentación y a las páginas de ejemplo para el servicio de imágenes, el procesamiento de imágenes y los visores de Scene7 (si están instalados).

## IS::CacheServerUrl - Dirección Url Raíz Del Servicio De Almacenamiento En Caché {#section-bcca227a1f91453b834db4ea050968e2}

Especifica la ruta raíz HTTP para permitir el acceso del servidor de imágenes al servicio de almacenamiento en caché. Debe configurarse en [!DNL http://localhost:TC::PsPort /is/cache/secondary], con el número de puerto que coincida con `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - TTL predeterminado de origen de imagen remota {#section-e4c31228b459492cacd2f482d9575f71}

TTL para imágenes en caché obtenidas mediante HTTP desde un origen remoto mediante la construcción `src={…}`. Solo se utiliza cuando el servidor remoto no incluye un encabezado de caducidad en su respuesta HTTP. Valor entero en segundos.

## IS::RemoteUrlTimeout - Tiempo de espera de origen de imagen remota {#section-437646c479cc4bea81dae42100a3c50a}

Tiempo que el servidor de imágenes esperará a que un servidor remoto entregue el archivo de imagen solicitado mediante HTTP antes de devolver un error. Valor entero en segundos.

## PS::allowDefaultCatalogRequests - Habilitar/deshabilitar solicitudes de catálogo predeterminadas {#section-484e442a115a49b4ac269d1718b351e1}

Establezca en false para no permitir solicitudes que no incluyan un ID de catálogo válido en la ruta. El valor predeterminado es `true`. Cuando se establece en `false`, se devuelve un error en las solicitudes sin un id. de catálogo.

>[!NOTE]
>
>`req=catalogprops` no está sujeto a esta configuración.

## PS::saveToFile.saveTimeout - Tiempo de espera para guardar archivos {#section-d22afd8ad86144b28684ed95a59db40e}

Valor de tiempo de espera predeterminado para `req=saveToFile` cuando `timeout=`no se especifica. `msec`. Se mostrará un error si la operación de guardado no se ha completado en el tiempo especificado.
