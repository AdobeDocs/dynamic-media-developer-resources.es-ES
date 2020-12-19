---
description: Debe configurar y configurar el módulo de compatibilidad IR 3.x.
seo-description: Debe configurar y configurar el módulo de compatibilidad IR 3.x.
seo-title: Configurar y configurar el módulo de compatibilidad IR 3.x
solution: Experience Manager
title: Configurar y configurar el módulo de compatibilidad IR 3.x
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# Configurar y configurar el módulo de compatibilidad de IR 3.x{#setup-and-configure-ir-x-compatibility-module}

Debe configurar y configurar el módulo de compatibilidad IR 3.x.

1. Detener `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Cambie al directorio de aplicaciones web de ImageServer.
1. Copie el contenido del directorio [!DNL ir] en el directorio [!DNL ROOT].
1. Abra [!DNL ROOT/WEB-INF/web.xml] en un editor de texto.
1. Buscar la línea `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Quite los comentarios de las etiquetas `<servlet>` y `<servlet-mapping>`.
1. Reiniciar `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Ejemplo de Linux**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

A continuación, edite [!DNL web.xml]con su editor favorito para eliminar los comentarios de las etiquetas `<servlet>` y `<servlet-mapping>`.

**Ejemplo de Windows**

Abra el Explorador y vaya a `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Seleccione todos los archivos y carpetas y cópielos dentro de `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

A continuación, edite el archivo `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml` sin comentar las etiquetas `<servlet>` y `<servlet-mapping>`.
