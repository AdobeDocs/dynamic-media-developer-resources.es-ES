---
title: Catálogos de materiales
description: Los catálogos de materiales ofrecen varias características.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
TQID: 'https://experienceleague.adobe.com/0ALFMea9A1hJtuPr3vG0cd34S-cLfTUNUGpIXZBpZBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 0%

---

# Catálogos de materiales {#material-catalogs}

Los catálogos de materiales ofrecen varias características.

* Permitir la definición persistente de materiales, incluidas todas las propiedades de los materiales.

  Se puede hacer referencia a los materiales definidos en el catálogo de materiales mediante una ID simple, en lugar de un conjunto de propiedades de material.
* Proporcione valores predeterminados para determinados atributos de solicitud, como la calidad de JPEG o un tamaño de imagen de respuesta predeterminado.
* Administre viñetas, perfiles ICC y plantillas de solicitud.

Aunque no se definan catálogos de material específicos, todas las características de los catálogos de material están disponibles a través del catálogo predeterminado ( [!DNL default.ini]).

Aunque los materiales de procesamiento pueden especificarse explícitamente en solicitudes que utilizan atributos de material, a menudo es más deseable ocultar los detalles de los materiales del sitio web utilizando catálogos de materiales. los comandos src= aceptan referencias de catálogo en lugar de rutas de archivo explícitas. Una entrada del catálogo consta de ` [ *[!DNL catId]*/] *[!DNL itemId]*`, donde ` *[!DNL catId]*` identifica un catálogo de materiales y ` *[!DNL itemId]*` identifica un registro del catálogo. Si no se especifica ` *[!DNL catId]*`, se utilizará el catálogo de sesiones (ver a continuación).

Un registro de catálogo coincide correctamente si (a) ` *[!DNL catId]*` coincide con el valor `attribute::RootId` de un catálogo de materiales y (b) ` *[!DNL recId]*` coincide con el valor catalog::Id del mismo catálogo. Si se encuentra una coincidencia correcta, los atributos del material (incluido `src=`) se establecen en los datos del registro de catálogo. Si el SMS incluye atributos adicionales para este material además de src=, anulan los valores del registro de catálogo.

Si ` *[!DNL recId]*` no coincide con una entrada de catálogo, ` *[!DNL catId]*` se reemplaza con `attribute::RootPath` del catálogo y la ruta de acceso resultante se supone que es una ruta de acceso de archivo simple. Otros atributos predeterminados (por ejemplo, `attribute::Resolution`) también se pueden heredar del catálogo de materiales.

Las viñetas y los perfiles ICC se pueden desglosar en catálogos de materiales similares a los propios materiales, y se les pueden dar propiedades. Además, el mapa de viñetas también proporciona el contenedor para las plantillas.

**Ver también**

Referencia de catálogo de materiales, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`

