---
description: Los catálogos de materiales ofrecen varias funciones.
seo-description: Los catálogos de materiales ofrecen varias funciones.
seo-title: Catálogos de materiales *
solution: Experience Manager
title: Catálogos de materiales *
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Catálogos de materiales *{#material-catalogs}

Los catálogos de materiales ofrecen varias funciones.

* Permitir la definición persistente de materiales, incluidas todas las propiedades materiales.

   Se puede hacer referencia a los materiales definidos en el catálogo de materiales mediante un ID simple, en lugar de un conjunto de propiedades de material.
* Proporcione valores predeterminados para ciertos atributos de solicitud, como la calidad JPEG o un tamaño de imagen de respuesta predeterminado.
* Administre viñetas, perfiles ICC y plantillas de solicitud.

Aunque no se definan catálogos de material específicos, todas las características de los catálogos de material están disponibles a través del catálogo predeterminado ( [!DNL default.ini]).

Aunque los materiales de procesamiento pueden especificarse explícitamente en las solicitudes utilizando atributos de material, en muchos casos es más conveniente ocultar los detalles de los materiales del sitio en la Web utilizando catálogos de materiales. los comandos src= aceptan referencias de catálogo en lugar de rutas de archivo explícitas. Una entrada de catálogo consta de ` [ *[!DNL catId]*/] *[!DNL itemId]*`, donde ` *[!DNL catId]*` identifica un catálogo de material y ` *[!DNL itemId]*` identifica un registro del catálogo. Si no se especifica ` *[!DNL catId]*`, se utiliza el catálogo de sesiones (consulte a continuación).

Un registro de catálogo coincide correctamente si (a) ` *[!DNL catId]*` coincide con el valor `attribute::RootId` de un catálogo de material y (b) ` *[!DNL recId]*` coincide con el valor de catálogo::Id del mismo catálogo. Si la coincidencia se realiza correctamente, los atributos del material (incluido `src=`) se establecen en los datos del registro de catálogo. Si el MSS incluye atributos adicionales para este material además de src=, anulan los valores del registro de catálogo.

Si ` *[!DNL recId]*` no coincide con una entrada de catálogo, ` *[!DNL catId]*` se reemplaza por `attribute::RootPath` del catálogo y la ruta resultante se asume como una ruta de archivo simple. Otros atributos predeterminados (p. ej. `attribute::Resolution`) también puede heredarse del catálogo de materiales.

Las viñetas y los perfiles ICC pueden desglosarse en catálogos de materiales similares a los materiales en sí y en determinadas propiedades. Además, el mapa de viñetas también proporciona el contenedor para plantillas.

**Véase también**

Referencia del catálogo de materiales, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
