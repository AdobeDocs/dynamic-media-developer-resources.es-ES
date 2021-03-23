---
description: Solo Platform Server accede a los archivos de datos de origen de contenido estático.
seo-description: Solo Platform Server accede a los archivos de datos de origen de contenido estático.
seo-title: Datos de fuente de contenido estático
solution: Experience Manager
title: Datos de fuente de contenido estático
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Datos de origen de contenido estático{#static-content-source-data}

Solo Platform Server accede a los archivos de datos de origen de contenido estático.

La ruta para los archivos de datos de contenido estático se resuelve de la siguiente manera:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

El servidor combina los segmentos de ruta de acceso de derecha a izquierda hasta que se establezca una ruta de archivo absoluta.

Todos los segmentos ` *[!DNL rootPath]*` pueden ser segmentos de ruta vacíos, relativos o absolutos.

` *[!DNL catalogPath]*` es una ruta/nombre de archivo absoluta o relativa. *[!DNL requestPath]* debe ser una ruta/nombre de archivo relativa.

Se pueden definir varios valores `PS::staticContent.rootPaths` en [!DNL PlatformServer.conf]. Esto permite distribuir los archivos de datos de origen entre varios sistemas de archivos. Platform Server intentará rutas alternativas en el orden especificado hasta que se encuentre el archivo de datos.
