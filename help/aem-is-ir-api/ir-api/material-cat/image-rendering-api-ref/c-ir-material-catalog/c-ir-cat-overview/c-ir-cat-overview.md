---
description: Los catálogos de materiales proporcionan al servidor información sobre viñetas, materiales y datos de apoyo, como perfiles ICC.
solution: Experience Manager
title: Descripción general del catálogo de materiales *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---


# Descripción general del catálogo de materiales *{#material-catalog-overview}

Los catálogos de materiales proporcionan al servidor información sobre viñetas, materiales y datos de apoyo, como perfiles ICC.

Cada catálogo de material consta de un *archivo de atributos de catálogo* requerido y un conjunto de *archivos de datos de catálogo* opcionales:

* El archivo de mapa de viñetas, que contiene viñetas y plantillas y sus metadatos asociados.
* El archivo de datos de material, que representa los materiales y especifica los archivos y metadatos de imagen de textura asociados.
* El archivo de definiciones de macro, que proporciona definiciones para las macros de solicitud.
* El archivo de mapa de perfiles, que representa los perfiles de color ICC.

Los archivos de datos del catálogo están asociados a catálogos de material por referencias de archivo en el archivo de atributos del catálogo. El mismo archivo de datos de catálogo se puede compartir mediante varios catálogos de material.

Los archivos de atributos del catálogo deben tener un sufijo de archivo [!DNL .ini] y deben estar ubicados en la carpeta *catalog folder* ( [!DNL PlatformServer::ir.catalogRootPath]) de procesamiento de imágenes. Los archivos de datos del catálogo se pueden encontrar en la misma carpeta o en cualquier otra carpeta accesible al servidor de procesamiento.

**Actualización de catálogos de material**

El servidor supervisa continuamente la carpeta del catálogo y vuelve a cargar automáticamente un catálogo de materiales, incluidos los archivos de datos del catálogo asociados, cuando detecta que se ha cambiado el archivo de atributos del catálogo principal. Por lo tanto, para actualizar los catálogos de materiales en el servidor, en primer lugar reemplace todos los archivos de datos del catálogo que deban cambiarse y, a continuación, sustituya (o &quot;toque&quot;) el archivo de atributos del catálogo para almacenar en déclencheur la recarga del catálogo.

**Catálogo predeterminado**

El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo de todos los catálogos de material. Si no se encuentra un atributo en particular en un catálogo de material específico, el servidor utilizará el valor correspondiente del catálogo predeterminado en su lugar. Del mismo modo, el catálogo predeterminado puede utilizarse para proporcionar valores predeterminados para registros de datos de catálogo específicos (materiales y perfiles ICC). Si no se encuentra un registro de datos concreto en un catálogo de materiales específico, el servidor intentará encontrarlo en el catálogo predeterminado. Esto permite que los catálogos de materiales se rellenen escasamente y simplifica la administración de atributos y datos globales, como plantillas compartidas, macros, fuentes, etc.

Además, el catálogo predeterminado proporciona todos los atributos y registros de datos (perfiles ICC) cuando no hay ningún catálogo de material específico involucrado en una operación.

Para el correcto funcionamiento del servidor de procesamiento, el archivo de atributos de catálogo para el catálogo predeterminado debe llamarse [!DNL default.ini], siempre debe existir en la carpeta del catálogo y debe rellenarse completamente con todos los atributos requeridos, excluyendo `attribute::RootId` y las referencias a los distintos archivos de datos del catálogo, que son todos opcionales.

**Véase también**

`PlatformServer::ir.catalogRootPath`
