---
description: Solo  [!DNL Platform Server] tiene acceso a los archivos de datos de origen de contenido estático.
solution: Experience Manager
title: Datos de origen de contenido estático
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
TQID: 'https://experienceleague.adobe.com/XFhKuqGPsarkFZcYcBo7XuyCEsiJINf-o6koIZQKAXU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# Datos de origen de contenido estático{#static-content-source-data}

Solo el [!DNL Platform Server] tiene acceso a los archivos de datos de origen de contenido estático.

La ruta para los archivos de datos de contenido estático se resuelve de la siguiente manera:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

El servidor combina los segmentos de ruta de derecha a izquierda hasta que se establece una ruta de archivo absoluta.

Todos los ` *[!DNL rootPath]*` segmentos pueden ser segmentos de ruta vacíos, relativos o absolutos.

` *[!DNL catalogPath]*` es una ruta de acceso o un nombre de archivo absoluto o relativo. *[!DNL requestPath]* debe ser una ruta de acceso/nombre de archivo relativo.

Se pueden definir varios valores `PS::staticContent.rootPaths` en [!DNL PlatformServer.conf]. Esto permite distribuir los archivos de datos de origen entre varios sistemas de archivos. [!DNL Platform Server] intenta usar rutas alternativas en el orden especificado hasta que se encuentra el archivo de datos.
