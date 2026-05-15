---
description: En esta documentación se explica cómo administrar el servidor de procesamiento de imágenes de Dynamic Media.
solution: Experience Manager
title: Resumen de administración del servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
TQID: 'https://experienceleague.adobe.com/t9zGehwMxhHq1HrP3mmNGvkthmqYxX2ijeyihn5OEWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# Resumen de administración del servidor{#server-administration-overview}

En esta documentación se explica cómo administrar el servidor de procesamiento de imágenes de Dynamic Media.

El procesamiento de imágenes consta de dos componentes principales:

* Se implementó un paquete Java con el servicio de imágenes [!DNL Platform Server] y se administró la conexión del cliente, el almacenamiento en caché y los catálogos de materiales.
* Un módulo de código nativo se implementa como una biblioteca de extensiones para el servidor de imágenes e implementa las funcionalidades principales de procesamiento de imágenes.

Ambos componentes se denominan colectivamente *Servidor de procesamiento*.

El procesamiento de imágenes comparte muchas funciones de servidor con el servicio de imágenes y todas las opciones se configuran editando un archivo de configuración. El catálogo predeterminado ([!DNL default.ini]) o catálogos de material específicos proporcionan atributos de configuración adicionales. Consulte Catálogos de materiales para obtener más información.

La carpeta de instalación de procesamiento de imágenes (*[!DNL install_folder]*) es [!DNL *[!DNL install_root]*/ImageRendering]. En Windows, el valor predeterminado *[!DNL install_root]* es `C:\Program Files\Scene7`. Se puede especificar una carpeta diferente durante la instalación. En Linux, *[!DNL install_root]* siempre debe ser [!DNL /usr/local/scene7]. Se pueden utilizar vínculos simbólicos.

Todas las rutas de archivo distinguen entre mayúsculas y minúsculas en UNIX y en Windows.
