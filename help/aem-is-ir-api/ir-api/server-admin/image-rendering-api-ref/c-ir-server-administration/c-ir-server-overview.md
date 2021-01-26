---
description: En esta documentación se explica cómo administrar el servidor de procesamiento de imágenes de Dynamic Media.
seo-description: En esta documentación se explica cómo administrar el servidor de procesamiento de imágenes de Dynamic Media.
seo-title: Información general sobre la administración de servidores
solution: Experience Manager
title: Información general sobre la administración de servidores
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# Información general sobre la administración de servidores{#server-administration-overview}

En esta documentación se explica cómo administrar el servidor de procesamiento de imágenes de Dynamic Media.

El procesamiento de imágenes consta de dos componentes principales:

* Un paquete de Java se implementa con el servidor de plataformas de servicio de imágenes y administra la conexión de clientes, el almacenamiento en caché y los catálogos de materiales.
* Un módulo de código nativo se implementa como una biblioteca de extensión para el servidor de imágenes e implementa las funciones principales de representación de imágenes.

Ambos componentes se denominan colectivamente *Servidor de procesamiento*.

El procesamiento de imágenes comparte muchas instalaciones de servidor con el servicio de imágenes y todas las opciones se configuran editando un archivo de configuración. El catálogo predeterminado ( [!DNL default.ini]) o los catálogos de material específicos proporcionan atributos de configuración adicionales. Consulte Catálogos de materiales para obtener más información.

La carpeta de instalación de procesamiento de imágenes ( *[!DNL install_folder]*) es [!DNL *[!DNL install_root]*/ImageRendering]. En Windows, el valor predeterminado *[!DNL install_root]* es `C:\Program Files\Scene7`. Se puede especificar una carpeta diferente durante la instalación. En Linux, *[!DNL install_root]* siempre debe ser [!DNL /usr/local/scene7]. Pueden utilizarse enlaces simbólicos.

Todas las rutas de archivos distinguen entre mayúsculas y minúsculas en UNIX y, en Windows, no distinguen entre mayúsculas y minúsculas.
