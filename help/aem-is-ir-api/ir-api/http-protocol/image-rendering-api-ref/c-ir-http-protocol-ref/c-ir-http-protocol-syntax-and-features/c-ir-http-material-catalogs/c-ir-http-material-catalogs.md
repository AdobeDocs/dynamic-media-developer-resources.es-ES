---
title: Catálogos de materiales
description: Los catálogos de materiales ofrecen varias características.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Catálogos de materiales {#material-catalogs}

Los catálogos de materiales ofrecen varias características.

* Permitir la definición persistente de materiales, incluidas todas las propiedades de los materiales.

  Se puede hacer referencia a los materiales definidos en el catálogo de materiales mediante una ID simple, en lugar de un conjunto de propiedades de material.
* Proporcione valores predeterminados para determinados atributos de solicitud, como la calidad JPEG o un tamaño de imagen de respuesta predeterminado.
* Administre viñetas, perfiles ICC y plantillas de solicitud.

Aunque no se definan catálogos de material específicos, todas las características de los catálogos de material están disponibles a través del catálogo predeterminado ( [!DNL default.ini]).

Aunque los materiales de procesamiento pueden especificarse explícitamente en solicitudes que utilizan atributos de material, a menudo es más deseable ocultar los detalles de los materiales del sitio web utilizando catálogos de materiales. los comandos src= aceptan referencias de catálogo en lugar de rutas de archivo explícitas. Una entrada del catálogo consta de ` [ *[!DNL catId]*/] *[!DNL itemId]*`, donde ` *[!DNL catId]*` identifica un catálogo de materiales y ` *[!DNL itemId]*` identifica un registro del catálogo. Si no se especifica ` *[!DNL catId]*`, se utilizará el catálogo de sesiones (ver a continuación).

Un registro de catálogo coincide correctamente si (a) ` *[!DNL catId]*` coincide con el valor `attribute::RootId` de un catálogo de materiales y (b) ` *[!DNL recId]*` coincide con el valor catalog::Id del mismo catálogo. Si se encuentra una coincidencia correcta, los atributos del material (incluido `src=`) se establecen en los datos del registro de catálogo. Si el SMS incluye atributos adicionales para este material además de src=, anulan los valores del registro de catálogo.

Si ` *[!DNL recId]*` no coincide con una entrada de catálogo, ` *[!DNL catId]*` se reemplaza con `attribute::RootPath` del catálogo y la ruta de acceso resultante se supone que es una ruta de acceso de archivo simple. Otros atributos predeterminados (por ejemplo, `attribute::Resolution`) también se pueden heredar del catálogo de materiales.

Las viñetas y los perfiles ICC se pueden desglosar en catálogos de materiales similares a los propios materiales, y se les pueden dar propiedades. Además, el mapa de viñetas también proporciona el contenedor para las plantillas.

**Ver también**

Referencia de catálogo de materiales, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
