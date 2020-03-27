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

---


# Catálogos de materiales *{#material-catalogs}

Los catálogos de materiales oferta varias funciones.

* Permitir una definición persistente de los materiales, incluidas todas las propiedades materiales.

   Se puede hacer referencia a los materiales definidos en el catálogo de materiales utilizando un ID sencillo, en lugar de un conjunto de propiedades materiales.
* Proporcione valores predeterminados para determinados atributos de solicitud, como la calidad JPEG o un tamaño de imagen de respuesta predeterminado.
* Administre viñetas, perfiles ICC y plantillas de solicitud.

Aunque no se definan catálogos de material específicos, todas las funciones de los catálogos de material están disponibles a través del catálogo predeterminado ( [!DNL default.ini]).

Si bien los materiales de procesamiento pueden especificarse explícitamente en las solicitudes utilizando atributos materiales, en muchos casos es más conveniente ocultar los detalles de los materiales del sitio Web utilizando catálogos materiales. los comandos src= aceptan referencias de catálogo en lugar de rutas de archivos explícitas. Una entrada de catálogo consiste en ` [ *[!DNL catId]*/] *[!DNL itemId]*`, donde ` *[!DNL catId]*` identifica un catálogo de materiales e ` *[!DNL itemId]*` identifica un registro del catálogo. Si no ` *[!DNL catId]*` se especifica, se utiliza el catálogo de sesiones (véase más abajo).

Un registro de catálogo coincide correctamente si (a) ` *[!DNL catId]*` coincide con el `attribute::RootId` valor de un catálogo de material y (b) ` *[!DNL recId]*` coincide con el valor de catálogo::Id del mismo catálogo. En caso de que la coincidencia sea satisfactoria, los atributos del material (incluidos `src=`) se establecen en los datos del registro del catálogo. Si el MSS incluye atributos adicionales para este material además de src=, anulan los valores del registro del catálogo.

Si ` *[!DNL recId]*` no se puede hacer coincidir con una entrada de catálogo, entonces ` *[!DNL catId]*` se reemplaza por `attribute::RootPath` desde el catálogo y se asume que la ruta resultante es una ruta de archivo simple. Otros atributos predeterminados (p. ej. `attribute::Resolution`) también puede heredarse del catálogo de materiales.

Las viñetas y los perfiles ICC se pueden desglosar en catálogos de materiales similares a los materiales en sí y con determinadas propiedades. Además, el mapa de viñetas también proporciona el contenedor para las plantillas.

**Véase también**

Referencia del catálogo de materiales, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
