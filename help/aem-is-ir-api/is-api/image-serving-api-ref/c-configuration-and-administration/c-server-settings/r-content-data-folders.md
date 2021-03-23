---
description: Utilice esta configuración del servidor para carpetas de datos de contenido.
seo-description: Utilice esta configuración del servidor para carpetas de datos de contenido.
seo-title: Carpetas de datos de contenido
solution: Experience Manager
title: Carpetas de datos de contenido
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# Carpetas de datos de contenido{#content-data-folders}

Utilice esta configuración del servidor para carpetas de datos de contenido.

## IS::RootPath - Carpetas raíz de datos de imagen {#section-5c57569514bb4d00b19de31d2e137e3b}

La ubicación de todos los datos de origen, incluidas las imágenes, las fuentes y los perfiles ICC. Puede ser una o más rutas de archivo absolutas o rutas relativas a *[!DNL install_folder]*, separadas por punto y coma. Si está vacío, *[!DNL install_folder]* es la raíz predeterminada. Se pueden especificar varios valores para distribuir los datos de imagen entre varios sistemas de archivos. El servidor de imágenes intentará las rutas raíz en el orden especificado hasta encontrar el archivo solicitado.

## PS::staticContent.rootPath: carpetas raíz de datos de contenido estático {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

La ubicación de los datos de origen de contenido estático que se pretende enviar mediante el contexto [!DNL /is/static]. Puede ser una o más rutas de archivo absolutas o rutas relativas a *[!DNL install_folder]*, separadas por punto y coma. Si está vacío, *[!DNL install_folder]* es la raíz predeterminada.

Se pueden especificar varios valores separados por punto y coma para distribuir contenido estático en varios sistemas de archivos. Normalmente se establece en los mismos valores que `IS::RootPath`.

Platform Server prueba las rutas raíz en el orden especificado hasta encontrar el archivo solicitado.

>[!NOTE]
>
>De forma predeterminada, este campo se establece intencionadamente en una ubicación no existente ( [!DNL *[!DNL install_folder]*/static]), lo que deshabilita de forma efectiva el servicio de contenido estático.

## IS::SaveDirectory - Archivo Guardar carpeta raíz {#section-1c517f8d49ce4cb8b9013e520bf309c9}

La ruta raíz para `attribute::SavePath` (utilizada por `req=saveToFile`). El servidor de imágenes debe tener permisos de acceso de creación para la subcarpeta en la que creará archivos de imagen.
