---
description: Utilice esta configuración del servidor para las carpetas de datos de contenido.
seo-description: Utilice esta configuración del servidor para las carpetas de datos de contenido.
seo-title: Carpetas de datos de contenido
solution: Experience Manager
title: Carpetas de datos de contenido
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# Carpetas de datos de contenido{#content-data-folders}

Utilice esta configuración del servidor para las carpetas de datos de contenido.

## IS::RootPath - Carpetas raíz de datos de imagen {#section-5c57569514bb4d00b19de31d2e137e3b}

Ubicación de todos los datos de origen, incluidas las imágenes, las fuentes y los perfiles ICC. Puede ser una o más rutas absolutas de archivos o rutas relativas a *[!DNL install_folder]*, separadas por punto y coma. Si está vacío, *[!DNL install_folder]* es la raíz predeterminada. Se pueden especificar varios valores para distribuir datos de imagen en varios sistemas de archivos. El servidor de imágenes intentará las rutas raíz en el orden especificado hasta que se encuentre el archivo solicitado.

## PS::staticContent.rootPath - Carpetas raíz de datos de contenido estático {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

La ubicación de los datos de fuentes de contenido estático que se va a entregar a través del contexto [!DNL /is/static]. Puede ser una o más rutas absolutas de archivos o rutas relativas a *[!DNL install_folder]*, separadas por punto y coma. Si está vacío, *[!DNL install_folder]* es la raíz predeterminada.

Se pueden especificar varios valores separados por punto y coma para distribuir contenido estático en varios sistemas de archivos. Generalmente se configura en los mismos valores que `IS::RootPath`.

Platform Server prueba las rutas raíz en el orden especificado hasta que se encuentra el archivo solicitado.

>[!NOTE]
>
>De forma predeterminada, este campo se establece intencionalmente en una ubicación no existente ( [!DNL *[!DNL install_folder]*/static]), lo que deshabilita de forma efectiva el servicio de contenido estático.

## IS::SaveDirectory - Archivo Guardar carpeta raíz {#section-1c517f8d49ce4cb8b9013e520bf309c9}

La ruta raíz para `attribute::SavePath` (utilizada por `req=saveToFile`). El servidor de imágenes debe tener permisos de acceso de creación para la subcarpeta en la que creará archivos de imagen.
