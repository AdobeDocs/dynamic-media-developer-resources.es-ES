---
description: Solo se accede a los archivos de fuente de contenido estático mediante la función [!DNL Platform Server].
solution: Experience Manager
title: Datos de fuente de contenido estático
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Datos de fuente de contenido estático{#static-content-source-data}

Solo se accede a los archivos de fuente de contenido estático mediante la función [!DNL Platform Server].

La ruta para los archivos de datos de contenido estático se resuelve de la siguiente manera:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

El servidor combina los segmentos de ruta de acceso de derecha a izquierda hasta que se establezca una ruta de archivo absoluta.

Todo ` *[!DNL rootPath]*` los segmentos pueden estar vacíos, relativos o segmentos de ruta absoluta.

` *[!DNL catalogPath]*` es una ruta/nombre de archivo absoluta o relativa. *[!DNL requestPath]* debe ser una ruta/nombre de archivo relativa.

Múltiple `PS::staticContent.rootPaths` Los valores se pueden definir en [!DNL PlatformServer.conf]. Esto permite distribuir los archivos de datos de origen entre varios sistemas de archivos. La variable [!DNL Platform Server] intentará rutas alternativas en el orden especificado hasta que se encuentre el archivo de datos.
