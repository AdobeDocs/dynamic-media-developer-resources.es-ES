---
description: Los catálogos de materiales oferta varias funciones.
seo-description: Los catálogos de materiales oferta varias funciones.
seo-title: Catálogos de materiales *
solution: Experience Manager
title: Catálogos de materiales *
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Catálogos de materiales *{#material-catalogs}

Los catálogos de materiales oferta varias funciones.

* Permitir una definición persistente de los materiales, incluidas todas las propiedades materiales.

   Se puede hacer referencia a los materiales definidos en el catálogo de materiales utilizando un ID sencillo, en lugar de un conjunto de propiedades materiales.
* Proporcione valores predeterminados para determinados atributos de solicitud, como la calidad JPEG o un tamaño de imagen de respuesta predeterminado.
* Administre viñetas, perfiles ICC y plantillas de solicitud.

Aunque no se definan catálogos de material específicos, todas las características de los catálogos de material están disponibles a través del catálogo predeterminado ( [!DNL default.ini]).

Si bien los materiales de procesamiento pueden especificarse explícitamente en las solicitudes utilizando atributos materiales, en muchos casos es más conveniente ocultar los detalles de los materiales del sitio Web utilizando catálogos materiales. los comandos src= aceptan referencias de catálogo en lugar de rutas de archivos explícitas. Una entrada de catálogo consiste en ` [ *[!DNL catId]*/] *[!DNL itemId]*`, donde ` *[!DNL catId]*` identifica un catálogo de material y ` *[!DNL itemId]*` identifica un registro en el catálogo. Si no se especifica ` *[!DNL catId]*`, se utiliza el catálogo de sesiones (véase más adelante).

Un registro de catálogo coincide correctamente si (a) ` *[!DNL catId]*` coincide con el valor `attribute::RootId` de un catálogo de material y (b) ` *[!DNL recId]*` coincide con el valor de catálogo::Id del mismo catálogo. En caso de que una coincidencia sea satisfactoria, los atributos del material (incluso `src=`) se establecen en los datos del registro del catálogo. Si el MSS incluye atributos adicionales para este material además de src=, anulan los valores del registro del catálogo.

Si ` *[!DNL recId]*` no se puede hacer coincidir con una entrada de catálogo, ` *[!DNL catId]*` se reemplaza por `attribute::RootPath` del catálogo y se asume que la ruta resultante es una ruta de archivo simple. Otros atributos predeterminados (p. ej. `attribute::Resolution`) también puede heredarse del catálogo de materiales.

Las viñetas y los perfiles ICC se pueden desglosar en catálogos de materiales similares a los materiales en sí y con determinadas propiedades. Además, el mapa de viñetas también proporciona el contenedor para las plantillas.

**Véase también**

Referencia del catálogo de materiales, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
