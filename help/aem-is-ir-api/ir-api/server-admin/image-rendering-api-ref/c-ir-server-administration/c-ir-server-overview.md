---
description: En esta documentación se explica cómo administrar el servidor de procesamiento de imágenes de Dynamic Media.
solution: Experience Manager
title: Resumen de administración del servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Resumen de administración del servidor{#server-administration-overview}

En esta documentación se explica cómo administrar el servidor de procesamiento de imágenes de Dynamic Media.

El procesamiento de imágenes consta de dos componentes principales:

* Se implementa un paquete Java con el servicio de imágenes [!DNL Platform Server] y gestiona la conexión del cliente, el almacenamiento en caché y los catálogos de material.
* Un módulo de código nativo se implementa como una biblioteca de extensiones para el servidor de imágenes e implementa las funcionalidades básicas de renderización de imágenes.

Ambos componentes se denominan colectivamente como *Servidor de procesamiento*.

Image Rendering comparte muchas instalaciones de servidor con Image Serving, y todas las opciones se configuran editando un archivo de configuración. El catálogo predeterminado proporciona atributos de configuración adicionales ( [!DNL default.ini]) o catálogos de materiales específicos. Consulte Catálogos de materiales para obtener más información.

La carpeta de instalación de renderización de imágenes ( *[!DNL install_folder]*) es [!DNL *[!DNL install_root]*/ImageRendering]. En Windows, el valor predeterminado *[!DNL install_root]* es `C:\Program Files\Scene7`. Se puede especificar una carpeta diferente durante la instalación. En Linux, *[!DNL install_root]* debe ser siempre [!DNL /usr/local/scene7]. Pueden utilizarse vínculos simbólicos.

Todas las rutas de archivos distinguen entre mayúsculas y minúsculas en UNIX y en Windows.
