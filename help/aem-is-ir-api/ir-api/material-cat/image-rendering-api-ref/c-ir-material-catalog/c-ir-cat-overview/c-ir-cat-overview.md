---
title: Resumen del catálogo de materiales
description: Los catálogos de materiales proporcionan información sobre viñetas, materiales y datos de apoyo, como perfiles ICC, al servidor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
TQID: 'https://experienceleague.adobe.com/wMShsstpVRBE4JNSUshejo0Qn6NXVB85YbLx5Pf9PEI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 0%

---

# Resumen del catálogo de materiales{#material-catalog-overview}

Los catálogos de materiales proporcionan información sobre viñetas, materiales y datos de apoyo, como perfiles ICC, al servidor.

Cada catálogo de materiales consta de un *archivo de atributos de catálogo* necesario y un conjunto de *archivos de datos de catálogo* opcionales:

* El archivo de mapa de viñetas, que muestra las viñetas y las plantillas y sus metadatos asociados.
* El archivo de datos de material, que detalla los materiales y especifica los archivos de imagen de textura y los metadatos asociados.
* El archivo de definiciones de macros, que proporciona definiciones para solicitar macros.
* El archivo de mapa de perfiles, que detalla los perfiles de color ICC.

Los ficheros de datos de catálogo se asocian a los catálogos de materiales mediante referencias de fichero en el fichero de atributos de catálogo. El mismo archivo de datos de catálogo se puede compartir con varios catálogos de materiales.

Los archivos de atributos de catálogo deben tener un sufijo de archivo [!DNL `.ini`] y deben estar en la carpeta *catalog* de procesamiento de imágenes ([!DNL PlatformServer::ir.catalogRootPath]). Los archivos de datos de catálogo pueden estar en la misma carpeta o en cualquier otra carpeta accesible para el servidor de procesamiento.

**Actualizando catálogos de material**

El servidor supervisa continuamente la carpeta del catálogo. Vuelve a cargar automáticamente un catálogo de materiales, incluidos los archivos de datos de catálogo asociados, cuando detecta que el archivo de atributos de catálogo principal se ha cambiado. Por lo tanto, para actualizar los catálogos de material en el servidor, reemplace primero todos los archivos de datos de catálogo que deban cambiarse y, a continuación, reemplace (o &quot;pulse&quot;) el archivo de atributos de catálogo para almacenar en déclencheur la recarga del catálogo.

**Catálogo predeterminado**

El catálogo por defecto proporciona valores por defecto para todos los atributos de catálogo para todos los catálogos de materiales. Si no se encuentra un atributo concreto en un catálogo de materiales específico, el servidor utiliza el valor correspondiente del catálogo por defecto. Del mismo modo, el catálogo predeterminado se puede utilizar para proporcionar valores predeterminados para registros de datos de catálogo específicos (materiales y perfiles ICC). Si no se encuentra un registro de datos concreto en un catálogo de materiales específico, el servidor intenta encontrarlo en el catálogo predeterminado en su lugar. Esto permite que los catálogos de material se rellenen escasamente y simplifica la administración de datos y atributos globales, como plantillas compartidas, macros y fuentes.

Además, el catálogo predeterminado proporciona todos los atributos y registros de datos (perfiles ICC) cuando no hay ningún catálogo de materiales específico involucrado en una operación.

Para que el servidor de procesamiento funcione correctamente, el archivo de atributos de catálogo del catálogo predeterminado debe llamarse [!DNL default.ini]. También debe existir siempre en la carpeta del catálogo y debe rellenarse completamente con todos los atributos necesarios, excluyendo `attribute::RootId` y las referencias a los distintos archivos de datos del catálogo, que son todos opcionales.

<!--
 **See also**

`PlatformServer::ir.catalogRootPath`
-->

