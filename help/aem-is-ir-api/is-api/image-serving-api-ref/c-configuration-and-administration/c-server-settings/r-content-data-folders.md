---
description: Utilice esta configuración del servidor para las carpetas de datos de contenido.
solution: Experience Manager
title: Carpetas de datos de contenido
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
TQID: 'https://experienceleague.adobe.com/IM1zNaaqC0zD36pUobHIL0Z-rlcrZoujnPbpBtOXq1Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 0%

---

# Carpetas de datos de contenido{#content-data-folders}

Utilice esta configuración del servidor para las carpetas de datos de contenido.

## IS::RootPath: carpetas raíz de datos de imagen {#section-5c57569514bb4d00b19de31d2e137e3b}

La ubicación de todos los datos de origen, incluidas imágenes, fuentes y perfiles ICC. Puede ser una o más rutas de acceso de archivo absolutas o rutas de acceso relativas a *[!DNL install_folder]*, separadas por punto y coma. Si está vacío, *[!DNL install_folder]* es la raíz predeterminada. Se pueden especificar varios valores para distribuir los datos de imagen entre varios sistemas de archivos. El servidor de imágenes prueba las rutas raíz en el orden especificado hasta que se encuentre el archivo solicitado.

## PS::staticContent.rootPath: carpetas raíz de datos de contenido estático {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

La ubicación de los datos de origen de contenido estático que se van a enviar mediante el contexto [!DNL /is/static]. Puede ser una o más rutas de acceso de archivo absolutas o rutas de acceso relativas a *[!DNL install_folder]*, separadas por punto y coma. Si está vacío, *[!DNL install_folder]* es la raíz predeterminada.

Se pueden especificar varios valores, separados por punto y coma, para distribuir el contenido estático entre varios sistemas de archivos. Normalmente se establece con los mismos valores que `IS::RootPath`.

El [!DNL Platform Server] prueba las rutas de acceso raíz en el orden especificado hasta que se encuentre el archivo solicitado.

>[!NOTE]
>
>De forma predeterminada, este campo se establece intencionadamente en una ubicación no existente ( [!DNL *[!DNL install_folder]*/static]), lo que deshabilita de forma efectiva el servicio de contenido estático.

## IS::SaveDirectory - Archivo Guardar carpeta raíz {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Ruta de acceso raíz de `attribute::SavePath` (usada por `req=saveToFile`). El servidor de imágenes debe tener permisos de creación de acceso para la subcarpeta en la que crea archivos de imagen.
