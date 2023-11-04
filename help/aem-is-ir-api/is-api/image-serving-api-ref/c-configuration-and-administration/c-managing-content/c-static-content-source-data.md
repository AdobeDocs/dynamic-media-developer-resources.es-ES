---
description: Solo se accede a los archivos de datos de origen de contenido estático mediante la variable [!DNL Platform Server].
solution: Experience Manager
title: Datos de origen de contenido estático
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Datos de origen de contenido estático{#static-content-source-data}

Solo se accede a los archivos de datos de origen de contenido estático mediante la variable [!DNL Platform Server].

La ruta para los archivos de datos de contenido estático se resuelve de la siguiente manera:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

El servidor combina los segmentos de ruta de derecha a izquierda hasta que se establece una ruta de archivo absoluta.

Todo ` *[!DNL rootPath]*` los segmentos pueden ser segmentos de ruta vacíos, relativos o absolutos.

` *[!DNL catalogPath]*` es una ruta de acceso o un nombre de archivo absoluto o relativo. *[!DNL requestPath]* debe ser una ruta/nombre de archivo relativo.

Múltiple `PS::staticContent.rootPaths` Los valores se pueden definir en [!DNL PlatformServer.conf]. Esto permite distribuir los archivos de datos de origen entre varios sistemas de archivos. El [!DNL Platform Server] intenta establecer rutas alternativas en el orden especificado hasta encontrar el archivo de datos.
