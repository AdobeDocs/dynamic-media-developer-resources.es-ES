---
title: Configurar el módulo de compatibilidad con IR 3.x
description: Configurar el módulo de compatibilidad con IR 3.x.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
TQID: 'https://experienceleague.adobe.com/ce7CdClFrrIFb7fhZRKQ7XBpsNm4BTgwVFHPXy3BXhw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 0%

---

# Configurar el módulo de compatibilidad con IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Detener `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Cambie al directorio de aplicaciones web de ImageServer.
1. Copie el contenido del directorio [!DNL ir] en el directorio [!DNL `ROOT`].
1. Abra [!DNL `ROOT/WEB-INF/web.xml`] en un editor de texto.
1. Busque la línea `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Quitar comentarios de las etiquetas `<servlet>` y `<servlet-mapping>`.
1. Reiniciar `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux® ejemplo**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

A continuación, edite [!DNL `web.xml`] con su editor favorito para quitar los comentarios de las etiquetas `<servlet>` y `<servlet-mapping>`.

**Ejemplo de Windows**

Abra el Explorador y vaya a `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Seleccione todos los archivos y carpetas y cópielos dentro de `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

A continuación, edite el archivo `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, sin comentar las etiquetas `<servlet>` y `<servlet-mapping>`.

