---
description: Los archivos de datos de origen de procesamiento de imágenes incluyen archivos de viñeta, archivos de material (imágenes para texturas y calcomanías repetibles, así como archivos de estilo de cubierta y ventana) y perfiles ICC.
solution: Experience Manager
title: Datos de Source
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Datos de Source{#source-data}

Los archivos de datos de origen de procesamiento de imágenes incluyen archivos de viñeta, archivos de material (imágenes para texturas y calcomanías repetibles, así como archivos de estilo de cubierta y ventana) y perfiles ICC.

Todos los archivos de datos de origen deben ser accesibles para el componente de código nativo del procesamiento de imágenes (ubicado junto con el servidor de imágenes).

Si hay un catálogo de materiales involucrado, el servidor de procesamiento busca el archivo especificado en el catálogo de materiales (con `vignette::Path`, `catalog::Path` o `icc::ProfilePath`) de la siguiente manera:

* Si la ruta es absoluta, se utiliza tal cual.
* Si la ruta es relativa, se le agregará el prefijo `catalog::RootPath` (de un catálogo de materiales con nombre).
* Si la ruta de acceso es absoluta, se utiliza; de lo contrario, se le agregará el prefijo `default::RootPath` (del catálogo predeterminado).
* Si la ruta es absoluta, se utiliza; de lo contrario, el servidor la combina con la ruta especificada en [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Si la ruta de acceso es ahora absoluta, se utiliza; de lo contrario, se supone que es relativa a [!DNL *[!DNL install_folder]*].

Si no hay ningún catálogo de imágenes involucrado, la ruta se combina con `default::RootPath` y luego se procesa como se indica arriba.

La ubicación física de los archivos de datos de origen se suele especificar con [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Se pueden especificar varios valores para permitir que los archivos de datos de origen se distribuyan en varios sistemas de archivos. El servidor de procesamiento intenta cada ruta en el orden especificado hasta que se encuentra el archivo de datos.

Se pueden agregar nuevos archivos de datos de cualquier tipo en cualquier momento sin detener el servidor.
