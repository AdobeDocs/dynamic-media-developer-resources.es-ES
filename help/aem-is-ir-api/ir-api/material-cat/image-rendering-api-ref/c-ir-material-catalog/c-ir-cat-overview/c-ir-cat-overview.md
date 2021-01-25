---
description: Los catálogos de materiales proporcionan al servidor información sobre viñetas, materiales y datos de soporte, como perfiles ICC.
seo-description: Los catálogos de materiales proporcionan al servidor información sobre viñetas, materiales y datos de soporte, como perfiles ICC.
seo-title: Descripción general del catálogo de materiales *
solution: Experience Manager
title: Descripción general del catálogo de materiales *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f2128b64-8caf-4a59-b11f-604fe62bae69
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---


# Descripción general del catálogo de materiales *{#material-catalog-overview}

Los catálogos de materiales proporcionan al servidor información sobre viñetas, materiales y datos de soporte, como perfiles ICC.

Cada catálogo de materiales consta de un *archivo de atributos de catálogo* requerido y un conjunto de *archivos de datos de catálogo* opcionales:

* El archivo de mapa de viñetas, que representa las viñetas y las plantillas y sus metadatos asociados.
* El archivo de datos de material, que representa los materiales y especifica los metadatos y archivos de imagen de textura asociados.
* El archivo de definiciones de macro, que proporciona definiciones para las macros de solicitud.
* El archivo de mapa de perfil, que representa los perfiles de color ICC.

Los archivos de datos del catálogo se asocian con los catálogos de material por referencias de archivo en el archivo de atributos del catálogo. El mismo archivo de datos de catálogo se puede compartir con varios catálogos de material.

Los archivos de atributos del catálogo deben tener un sufijo de archivo [!DNL .ini] y estar ubicados en la carpeta de procesamiento de imágenes *catálogo* ( [!DNL PlatformServer::ir.catalogRootPath]). Los archivos de datos del catálogo se pueden ubicar en la misma carpeta o en cualquier otra carpeta accesible para el servidor de procesamiento.

**Actualización de catálogos de material**

El servidor supervisa continuamente la carpeta del catálogo y vuelve a cargar automáticamente un catálogo de materiales, incluidos los archivos de datos del catálogo asociados, cuando detecta que se ha cambiado el archivo de atributos del catálogo principal. Por lo tanto, para actualizar los catálogos de material en el servidor, primero reemplace todos los archivos de datos del catálogo que deban cambiarse y, a continuación, reemplace (o &quot;toque&quot;) el archivo de atributos del catálogo para déclencheur de la recarga del catálogo.

**Catálogo predeterminado**

El catálogo predeterminado proporciona valores predeterminados para todos los atributos de catálogo de todos los catálogos de material. Si no se encuentra un atributo concreto en un catálogo de material específico, el servidor utilizará el valor correspondiente del catálogo predeterminado. Del mismo modo, el catálogo predeterminado se puede utilizar para proporcionar valores predeterminados para registros de datos de catálogo específicos (materiales y perfiles ICC). Si no se encuentra un registro de datos concreto en un catálogo de materiales específico, el servidor intentará encontrarlo en el catálogo predeterminado. Esto permite que los catálogos de materiales se rellenen con poca frecuencia y simplifica la administración de atributos y datos globales, como plantillas compartidas, macros, fuentes, etc.

Además, el catálogo predeterminado proporciona todos los atributos y registros de datos (perfiles ICC) cuando no hay ningún catálogo de material específico involucrado en una operación.

Para el correcto funcionamiento del servidor de procesamiento, el archivo de atributos del catálogo para el catálogo predeterminado debe tener el nombre [!DNL default.ini], debe existir siempre en la carpeta del catálogo y debe rellenarse con todos los atributos necesarios, excluyendo `attribute::RootId` y las referencias a los distintos archivos de datos del catálogo, que son todos opcionales.

**Véase también**

`PlatformServer::ir.catalogRootPath`
