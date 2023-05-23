---
title: Configurar el módulo de compatibilidad con IR 3.x
description: Configurar el módulo de compatibilidad con IR 3.x.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---

# Configurar el módulo de compatibilidad con IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Detener `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Cambie al directorio de aplicaciones web de ImageServer.
1. Copie el contenido del [!DNL ir] en el [!DNL `ROOT`] directorio.
1. Abrir [!DNL `ROOT/WEB-INF/web.xml`] en un editor de texto.
1. Buscar la línea `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Quitar comentarios de `<servlet>` y `<servlet-mapping>` etiquetas.
1. Reiniciar `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Ejemplo de Linux®**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

A continuación, editar [!DNL `web.xml`] uso de su editor favorito para quitar los comentarios del `<servlet>` y `<servlet-mapping>` etiquetas.

**Ejemplo de Windows**

Abra el Explorador y vaya a `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Seleccione todos los archivos y carpetas y cópielos dentro `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Luego edite el archivo `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, sin comentar `<servlet>` y `<servlet-mapping>` etiquetas.
