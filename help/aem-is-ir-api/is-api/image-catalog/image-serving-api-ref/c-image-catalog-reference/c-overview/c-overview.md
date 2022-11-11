---
description: Los catálogos de imágenes se utilizan para proporcionar información sobre imágenes y datos de apoyo (como fuentes y perfiles ICC) al servidor.
solution: Experience Manager
title: Información general
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Información general{#overview}

Los catálogos de imágenes se utilizan para proporcionar información sobre imágenes y datos de apoyo (como fuentes y perfiles ICC) al servidor.

Los catálogos de imágenes se utilizan para proporcionar información sobre imágenes y datos de apoyo (como fuentes y perfiles ICC) al servidor.

Cada catálogo de imágenes consta de un archivo de atributos de catálogo requerido y un conjunto de archivos de datos de catálogo opcionales:

* El archivo de datos de imagen, que representa las imágenes y plantillas y sus metadatos asociados.
* El archivo de datos del SVG, que representa los archivos del SVG y sus metadatos asociados.
* El archivo de definiciones de macro, que proporciona definiciones para las macros de solicitud.
* El archivo de mapa de fuentes, que realiza un seguimiento de las fuentes de texto.
* El archivo de mapa de perfiles, que representa los perfiles de color ICC.
* El archivo del conjunto de reglas, que define las reglas de preprocesamiento de solicitudes HTTP.

Los archivos de datos del catálogo están asociados a catálogos de imágenes por referencias de archivo en el archivo de atributos del catálogo. El mismo archivo de datos de catálogo se puede compartir en varios catálogos de imágenes.

Los archivos de atributos del catálogo deben tener un [!DNL .ini] y debe estar ubicado en el [!DNL Platform Server]La carpeta del catálogo ( `PlatformServer::catalog.rootPath`). Los archivos de datos del catálogo se pueden encontrar en la misma carpeta o en cualquier otra carpeta accesible para la [!DNL Platform Server].

Este documento describe el formato de archivo del Catálogo de imágenes para el sistema de servicio de imágenes de Dynamic Media. La audiencia deseada son programadores experimentados y desarrolladores de sitios web que desean aprovechar Dynamic Media Image Serving para una aplicación web o personalizada.

Se supone que el lector está familiarizado con el sistema de servicio de imágenes de Dynamic Media, las normas y convenciones generales de protocolo HTTP y la terminología básica de imágenes.
