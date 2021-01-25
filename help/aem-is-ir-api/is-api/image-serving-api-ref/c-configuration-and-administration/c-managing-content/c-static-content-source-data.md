---
description: El servidor de plataforma solo puede acceder a los archivos de datos de origen de contenido estático.
seo-description: El servidor de plataforma solo puede acceder a los archivos de datos de origen de contenido estático.
seo-title: Datos de fuente de contenido estático
solution: Experience Manager
title: Datos de fuente de contenido estático
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# Datos de origen de contenido estático{#static-content-source-data}

El servidor de plataforma solo puede acceder a los archivos de datos de origen de contenido estático.

La ruta para los archivos de datos de contenido estático se resuelve de la siguiente manera:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

El servidor combina segmentos de ruta de acceso de derecha a izquierda hasta que se establece una ruta absoluta de archivo.

Todos los segmentos ` *[!DNL rootPath]*` pueden estar vacíos, relativos o absolutos.

` *[!DNL catalogPath]*` es una ruta/nombre de archivo absoluta o relativa. *[!DNL requestPath]* debe ser una ruta/nombre de archivo relativa.

Se pueden definir varios valores `PS::staticContent.rootPaths` en [!DNL PlatformServer.conf]. Esto permite que los archivos de datos de origen se distribuyan en varios sistemas de archivos. Platform Server intentará rutas alternativas en el orden especificado hasta que se encuentre el archivo de datos.
