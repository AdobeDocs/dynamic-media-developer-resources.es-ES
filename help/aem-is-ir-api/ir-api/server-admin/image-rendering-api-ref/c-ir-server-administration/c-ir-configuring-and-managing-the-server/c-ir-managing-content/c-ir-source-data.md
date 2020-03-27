---
description: Los archivos de datos de origen de procesamiento de imágenes incluyen archivos de viñeta, archivos de material (imágenes para texturas y calcomanías repetibles, así como archivos de estilo de archivador y ventana) y perfiles ICC.
seo-description: Los archivos de datos de origen de procesamiento de imágenes incluyen archivos de viñeta, archivos de material (imágenes para texturas y calcomanías repetibles, así como archivos de estilo de archivador y ventana) y perfiles ICC.
seo-title: Datos de origen
solution: Experience Manager
title: Datos de origen
topic: Scene7 Image Serving - Image Rendering API
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Datos de origen{#source-data}

Los archivos de datos de origen de procesamiento de imágenes incluyen archivos de viñeta, archivos de material (imágenes para texturas y calcomanías repetibles, así como archivos de estilo de archivador y ventana) y perfiles ICC.

Todos los archivos de datos de origen deben ser accesibles para el componente de código nativo del procesamiento de imágenes (ubicado junto con el servidor de imágenes).

Si se trata de un catálogo de materiales, el servidor de procesamiento busca el archivo especificado en el catálogo de materiales (con `vignette::Path`, `catalog::Path`o `icc::ProfilePath`) de la siguiente manera:

* Si la ruta es absoluta, se utiliza tal cual.
* Si la ruta es relativa, lleva el prefijo `catalog::RootPath` (de un catálogo de materiales con nombre).
* Si la ruta es absoluta, se utiliza; en caso contrario, el prefijo es `default::RootPath` (del catálogo predeterminado).
* Si la ruta es absoluta, se utiliza; de lo contrario, el servidor lo combina con la ruta especificada en [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Si la ruta es ahora absoluta, se utiliza; de lo contrario, se supone que es relativa a [!DNL *[!DNL install_folder]*].

Si no hay ningún catálogo de imágenes involucrado, la ruta se combina con `default::RootPath` y luego se procesa como se muestra arriba.

La ubicación física de los archivos de datos de origen suele especificarse con [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Se pueden especificar varios valores para permitir que los archivos de datos de origen se distribuyan en varios sistemas de archivos. El servidor de procesamiento intentará cada ruta en el orden especificado hasta que se encuentre el archivo de datos.

Se pueden agregar nuevos archivos de datos de cualquier tipo en cualquier momento sin detener el servidor.
