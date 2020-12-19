---
description: Los catálogos de imágenes se utilizan para proporcionar al servidor información sobre las imágenes y los datos de apoyo (como las fuentes y los perfiles ICC).
seo-description: Los catálogos de imágenes se utilizan para proporcionar al servidor información sobre las imágenes y los datos de apoyo (como las fuentes y los perfiles ICC).
seo-title: Información general
solution: Experience Manager
title: Información general
topic: Scene7 Image Serving - Image Rendering API
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Información general{#overview}

Los catálogos de imágenes se utilizan para proporcionar al servidor información sobre las imágenes y los datos de apoyo (como las fuentes y los perfiles ICC).

Los catálogos de imágenes se utilizan para proporcionar al servidor información sobre las imágenes y los datos de apoyo (como las fuentes y los perfiles ICC).

Cada catálogo de imágenes consta de un archivo de atributos de catálogo requerido y un conjunto de archivos de datos de catálogo opcionales:

* El archivo de datos de imagen, que representa las imágenes y las plantillas y sus metadatos asociados.
* El archivo de datos SVG, que representa los archivos SVG y sus metadatos asociados.
* El archivo de definiciones de macro, que proporciona definiciones para las macros de solicitud.
* El archivo de asignación de fuentes, que realiza un seguimiento de las fuentes de texto.
* El archivo de mapa de perfil, que representa los perfiles de color ICC.
* El archivo de conjunto de reglas, que define las reglas de preprocesamiento de solicitudes HTTP.

Los archivos de datos del catálogo se asocian a los catálogos de imágenes mediante referencias de archivo en el archivo de atributos del catálogo. Varios catálogos de imágenes pueden compartir el mismo archivo de datos de catálogo.

Los archivos de atributos del catálogo deben tener un sufijo de archivo [!DNL .ini] y estar ubicados en la carpeta de catálogo de Platform Server ( `PlatformServer::catalog.rootPath`). Los archivos de datos del catálogo se pueden ubicar en la misma carpeta o en cualquier otra carpeta accesible para el servidor de plataforma.

Este documento describe el formato de archivo del catálogo de imágenes para el sistema Scene7 Image Serving. La audiencia deseada son programadores experimentados y desarrolladores de sitios web que desean aprovechar el servicio de imágenes de Scene7 para una aplicación web o personalizada.

Se supone que el lector está familiarizado generalmente con el sistema de servicio de imágenes de Scene7, las normas y convenciones generales del protocolo HTTP y la terminología básica de imágenes.
