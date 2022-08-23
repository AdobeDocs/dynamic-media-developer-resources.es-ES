---
title: Resumen del catálogo de materiales
description: Los catálogos de materiales proporcionan al servidor información sobre viñetas, materiales y datos de apoyo, como perfiles ICC.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Resumen del catálogo de materiales{#material-catalog-overview}

Los catálogos de materiales proporcionan al servidor información sobre viñetas, materiales y datos de apoyo, como perfiles ICC.

Cada catálogo de materiales consta de un *archivo de atributos de catálogo* y un conjunto de *archivos de datos de catálogo*:

* El archivo de mapa de viñetas, que contiene viñetas y plantillas y sus metadatos asociados.
* El archivo de datos de material, que representa los materiales y especifica los archivos y metadatos de imagen de textura asociados.
* El archivo de definiciones de macro, que proporciona definiciones para las macros de solicitud.
* El archivo de mapa de perfiles, que representa los perfiles de color ICC.

Los archivos de datos del catálogo están asociados a catálogos de material por referencias de archivo en el archivo de atributos del catálogo. El mismo archivo de datos de catálogo se puede compartir mediante varios catálogos de material.

Los archivos de atributos del catálogo deben tener un [!DNL `.ini`] sufijo de archivo y debe estar en Image Rendering *carpeta del catálogo* ( [!DNL PlatformServer::ir.catalogRootPath]). Los archivos de datos del catálogo pueden estar en la misma carpeta o en cualquier otra carpeta accesible al servidor de procesamiento.

**Actualización de catálogos de material**

El servidor supervisa continuamente la carpeta del catálogo. Automáticamente vuelve a cargar un catálogo de materiales (incluidos los archivos de datos del catálogo asociados) cuando detecta que se ha cambiado el archivo de atributos del catálogo principal. Por lo tanto, para actualizar los catálogos de materiales en el servidor, en primer lugar reemplace todos los archivos de datos del catálogo que deban cambiarse y, a continuación, sustituya (o &quot;toque&quot;) el archivo de atributos del catálogo para almacenar en déclencheur la recarga del catálogo.

**Catálogo predeterminado**

El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo de todos los catálogos de material. Si un atributo en particular no se encuentra en un catálogo de material específico, el servidor utiliza el valor correspondiente del catálogo predeterminado en su lugar. Del mismo modo, el catálogo predeterminado puede utilizarse para proporcionar valores predeterminados para registros de datos de catálogo específicos (materiales y perfiles ICC). Si no se encuentra un registro de datos concreto en un catálogo de materiales específico, el servidor intenta encontrarlo en el catálogo predeterminado. Esto permite que los catálogos de materiales se rellenen escasamente y simplifica la administración de atributos y datos globales, como plantillas compartidas, macros y fuentes.

Además, el catálogo predeterminado proporciona todos los atributos y registros de datos (perfiles ICC) cuando no hay ningún catálogo de material específico involucrado en una operación.

Para el correcto funcionamiento del servidor de procesamiento, se debe asignar un nombre al archivo de atributos de catálogo del catálogo predeterminado [!DNL default.ini]. También debe existir siempre en la carpeta del catálogo y debe rellenarse completamente con todos los atributos necesarios, excluyendo `attribute::RootId` y las referencias a los distintos archivos de datos del catálogo, que son opcionales.

<!-- **See also**

`PlatformServer::ir.catalogRootPath` -->
