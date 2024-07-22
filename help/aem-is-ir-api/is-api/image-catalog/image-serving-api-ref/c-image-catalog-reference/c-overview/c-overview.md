---
description: Los catálogos de imágenes se utilizan para proporcionar información sobre imágenes y datos de soporte (como fuentes y perfiles ICC) al servidor.
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

Los catálogos de imágenes se utilizan para proporcionar información sobre imágenes y datos de soporte (como fuentes y perfiles ICC) al servidor.

Los catálogos de imágenes se utilizan para proporcionar información sobre imágenes y datos de soporte (como fuentes y perfiles ICC) al servidor.

Cada catálogo de imágenes consta de un archivo de atributos de catálogo necesario y un conjunto de archivos de datos de catálogo opcionales:

* El archivo de datos de imagen, que detalla las imágenes y las plantillas y sus metadatos asociados.
* El archivo de datos del SVG, que detalla los archivos del SVG y sus metadatos asociados.
* El archivo de definiciones de macros, que proporciona definiciones para solicitar macros.
* El archivo de mapa de fuentes, que realiza un seguimiento de las fuentes de texto.
* El archivo de mapa de perfiles, que detalla los perfiles de color ICC.
* El archivo del conjunto de reglas, que define las reglas de preprocesamiento de solicitudes HTTP.

Los archivos de datos de catálogo se asocian a los catálogos de imágenes mediante referencias de archivo en el archivo de atributos de catálogo. Varios catálogos de imágenes pueden compartir el mismo archivo de datos de catálogo.

Los archivos de atributos de catálogo deben tener un sufijo de archivo [!DNL .ini] y deben estar ubicados en la carpeta de catálogo de [!DNL Platform Server] ( `PlatformServer::catalog.rootPath`). Los archivos de datos de catálogo se pueden encontrar en la misma carpeta o en cualquier otra carpeta a la que tenga acceso [!DNL Platform Server].

En este documento se describe el formato de archivo del catálogo de imágenes para el sistema de servicio de imágenes de Dynamic Media. La audiencia a la que se dirige son programadores con experiencia y desarrolladores de sitios web que desean aprovechar el servicio de imágenes de Dynamic Media para una aplicación web o personalizada.

Se da por hecho que el lector está familiarizado en general con el sistema de servicio de imágenes de Dynamic Media, las normas y convenciones generales del protocolo HTTP y la terminología básica de las imágenes.
