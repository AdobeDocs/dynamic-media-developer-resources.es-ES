---
description: Debe configurar el módulo de compatibilidad de IR 3.x.
solution: Experience Manager
title: Configuración y configuración del módulo de compatibilidad de IR 3.x
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 1%

---

# Configuración y configuración del módulo de compatibilidad de IR 3.x{#setup-and-configure-ir-x-compatibility-module}

Debe configurar el módulo de compatibilidad de IR 3.x.

1. Detener `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Cambie al directorio de aplicaciones web de ImageServer.
1. Copie el contenido del directorio [!DNL ir] en el directorio [!DNL ROOT].
1. Abra [!DNL ROOT/WEB-INF/web.xml] en un editor de texto.
1. Busque la línea `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Descomente las etiquetas `<servlet>` y `<servlet-mapping>` .
1. Reiniciar `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Ejemplo de Linux**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

A continuación, edite [!DNL web.xml]con su editor favorito para anular el comentario de las etiquetas `<servlet>` y `<servlet-mapping>` .

**Ejemplo de Windows**

Abra Explorer y vaya a `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Seleccione todos los archivos y carpetas y cópielos dentro de `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

A continuación, edite el archivo `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml` sin comentar las etiquetas `<servlet>` y `<servlet-mapping>` .
