---
description: Utilice esta configuración del servidor para las carpetas de datos de contenido.
seo-description: Utilice esta configuración del servidor para las carpetas de datos de contenido.
seo-title: Carpetas de datos de contenido
solution: Experience Manager
title: Carpetas de datos de contenido
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Carpetas de datos de contenido{#content-data-folders}

Utilice esta configuración del servidor para las carpetas de datos de contenido.

## IS::RootPath - Carpetas raíz de datos de imagen {#section-5c57569514bb4d00b19de31d2e137e3b}

Ubicación de todos los datos de origen, incluidas las imágenes, las fuentes y los perfiles ICC. Puede ser una o más rutas absolutas de archivos o rutas relativas a *[!DNL install_folder]*, separadas por punto y coma. Si está vacío, *[!DNL install_folder]* es la raíz predeterminada. Se pueden especificar varios valores para distribuir datos de imagen en varios sistemas de archivos. El servidor de imágenes intentará las rutas raíz en el orden especificado hasta que se encuentre el archivo solicitado.

## PS::staticContent.rootPath - Carpetas raíz de datos de contenido estático {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Ubicación de los datos de fuentes de contenido estático que se van a entregar a través del [!DNL /is/static] contexto. Puede ser una o más rutas absolutas de archivos o rutas relativas a *[!DNL install_folder]*, separadas con punto y coma. Si está vacío, *[!DNL install_folder]* es la raíz predeterminada.

Se pueden especificar varios valores separados por punto y coma para distribuir contenido estático en varios sistemas de archivos. Generalmente se establece en los mismos valores que `IS::RootPath`.

Platform Server prueba las rutas raíz en el orden especificado hasta que se encuentra el archivo solicitado.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>De forma predeterminada, este campo se establece intencionalmente en una ubicación no existente ( [!DNL *[!DNL install_folder]*/static]), lo que deshabilita de forma efectiva el servicio de contenido estático.

## IS::SaveDirectory - Archivo Guardar carpeta raíz {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Ruta de acceso raíz para `attribute::SavePath` (utilizada por `req=saveToFile`). El servidor de imágenes debe tener permisos de acceso de creación para la subcarpeta en la que creará archivos de imagen.
