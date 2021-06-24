---
description: Solo Platform Server accede a los archivos de datos de origen de contenido estático.
solution: Experience Manager
title: Datos de fuente de contenido estático
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Datos de fuente de contenido estático{#static-content-source-data}

Solo Platform Server accede a los archivos de datos de origen de contenido estático.

La ruta para los archivos de datos de contenido estático se resuelve de la siguiente manera:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

El servidor combina los segmentos de ruta de acceso de derecha a izquierda hasta que se establezca una ruta de archivo absoluta.

Todos los segmentos ` *[!DNL rootPath]*` pueden ser segmentos de ruta vacíos, relativos o absolutos.

` *[!DNL catalogPath]*` es una ruta/nombre de archivo absoluta o relativa. *[!DNL requestPath]* debe ser una ruta/nombre de archivo relativa.

Se pueden definir varios valores `PS::staticContent.rootPaths` en [!DNL PlatformServer.conf]. Esto permite distribuir los archivos de datos de origen entre varios sistemas de archivos. Platform Server intentará rutas alternativas en el orden especificado hasta que se encuentre el archivo de datos.
