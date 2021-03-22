---
description: En esta documentación se explica cómo administrar el servidor de procesamiento de imágenes de Dynamic Media.
seo-description: En esta documentación se explica cómo administrar el servidor de procesamiento de imágenes de Dynamic Media.
seo-title: Resumen de administración del servidor
solution: Experience Manager
title: Resumen de administración del servidor
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# Resumen de administración del servidor{#server-administration-overview}

En esta documentación se explica cómo administrar el servidor de procesamiento de imágenes de Dynamic Media.

El procesamiento de imágenes consta de dos componentes principales:

* Un paquete Java se implementa con Image Serving Platform Server y gestiona la conexión del cliente, el almacenamiento en caché y los catálogos de materiales.
* Un módulo de código nativo se implementa como una biblioteca de extensiones para el servidor de imágenes e implementa las funcionalidades básicas de renderización de imágenes.

Ambos componentes se denominan colectivamente *Render Server*.

Image Rendering comparte muchas instalaciones de servidor con Image Serving, y todas las opciones se configuran editando un archivo de configuración. El catálogo predeterminado ( [!DNL default.ini]) o catálogos de material específicos proporcionan atributos de configuración adicionales. Consulte Catálogos de materiales para obtener más información.

La carpeta de instalación de procesamiento de imágenes ( *[!DNL install_folder]*) es [!DNL *[!DNL install_root]*/ImageRendering]. En Windows, el *[!DNL install_root]* predeterminado es `C:\Program Files\Scene7`. Se puede especificar una carpeta diferente durante la instalación. En Linux, *[!DNL install_root]* siempre debe ser [!DNL /usr/local/scene7]. Pueden utilizarse vínculos simbólicos.

Todas las rutas de archivos distinguen entre mayúsculas y minúsculas en UNIX y en Windows.
