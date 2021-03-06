---
description: Los archivos de fuente de renderización de imágenes incluyen archivos de viñeta, archivos de material (imágenes para texturas y calcomanías repetibles, así como archivos de estilo de archivador y ventana) y perfiles ICC.
solution: Experience Manager
title: Datos de origen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Datos de origen{#source-data}

Los archivos de fuente de renderización de imágenes incluyen archivos de viñeta, archivos de material (imágenes para texturas y calcomanías repetibles, así como archivos de estilo de archivador y ventana) y perfiles ICC.

Todos los archivos de datos de origen deben ser accesibles para el componente de código nativo de Representación de imágenes (ubicado junto con el Servidor de imágenes).

Si hay un catálogo de materiales involucrado, el servidor de procesamiento busca el archivo especificado en el catálogo de materiales (con `vignette::Path`, `catalog::Path` o `icc::ProfilePath`) de la siguiente manera:

* Si la ruta es absoluta, se utiliza tal cual.
* Si la ruta es relativa, lleva el prefijo `catalog::RootPath` (de un catálogo de materiales con nombre).
* Si la ruta es absoluta, se utiliza; de lo contrario, lleva el prefijo `default::RootPath` (del catálogo predeterminado).
* Si la ruta es absoluta, se utiliza; de lo contrario, el servidor lo combina con la ruta especificada en [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Si la ruta es ahora absoluta, se utiliza; de lo contrario, se supone que es relativo a [!DNL *[!DNL install_folder]*].

Si no hay ningún catálogo de imágenes involucrado, la ruta se combina con `default::RootPath` y luego se procesa como se muestra arriba.

La ubicación física de los archivos de datos de origen generalmente se especifica con [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Se pueden especificar varios valores para permitir que los archivos de datos de origen se distribuyan entre varios sistemas de archivos. El servidor de procesamiento intentará cada ruta en el orden especificado hasta que se encuentre el archivo de datos.

Se pueden agregar nuevos archivos de datos de cualquier tipo en cualquier momento sin detener el servidor.
