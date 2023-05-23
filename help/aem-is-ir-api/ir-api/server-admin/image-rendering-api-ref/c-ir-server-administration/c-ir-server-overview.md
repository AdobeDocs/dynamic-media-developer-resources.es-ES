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

* Se implementa un paquete Java con el servicio de imágenes [!DNL Platform Server] y administra la conexión de cliente, el almacenamiento en caché y los catálogos de materiales.
* Un módulo de código nativo se implementa como una biblioteca de extensiones para el servidor de imágenes e implementa las funcionalidades principales de procesamiento de imágenes.

Ambos componentes se denominan colectivamente *Servidor de procesamiento*.

El procesamiento de imágenes comparte muchas funciones de servidor con el servicio de imágenes y todas las opciones se configuran editando un archivo de configuración. El catálogo predeterminado ( ) proporciona atributos de configuración adicionales [!DNL default.ini]) o catálogos de material específicos. Consulte Catálogos de materiales para obtener más información.

La carpeta de instalación del procesamiento de imágenes ( *[!DNL install_folder]*) es [!DNL *[!DNL install_root]*/ImageRendering]. En Windows, la opción predeterminada *[!DNL install_root]* es `C:\Program Files\Scene7`. Se puede especificar una carpeta diferente durante la instalación. En Linux, *[!DNL install_root]* siempre debe ser [!DNL /usr/local/scene7]. Se pueden utilizar vínculos simbólicos.

Todas las rutas de archivo distinguen entre mayúsculas y minúsculas en UNIX y en Windows.
